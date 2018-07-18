# matlab-engineering-codes
this will be about solving engineering problems on matlab 
# many aplication use the small angle approximation for the sine to obtain a simpler model
# that s easy to understand and analyze this approximation states that sinx =x, where x must be in radians 
# investigate the accuracyof this approximation by creating three plots: 

clear all ,clc ;
figure ;
x=0:0.01:1 ;                    % initiallizing the x value .
subplot(2,2,1);                 % divided the figure into 2 rows and two columns .
plot (x,sin(x),x,x,'--r') ;     % first plot .
xlabel('x (radius)');
ylabel('xand sin(x)');
gtext('x');
gtext('sin(x)');
subplot(2,2,2);
plot(x,abs(sin(x)-x));                          % second plot .
xlabel('x');
ylabel('error');
subplot(2,2,3);
plot(x,abs(100*(sin(x)-x))./sin(x));            % third plot .
xlabel('x');
ylabel('percent  error'); 
grid minor; 
 
