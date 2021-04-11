---
description: Abilita la scalabilità della porta locale per un socket.
ms.assetid: c5142baf-9e2d-4c06-8719-9090fd2d9487
title: SO_PORT_SCALABILITY (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565caeb472ac5cb15061d32b47a048a9a210885e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129119"
---
# <a name="so_port_scalability"></a>\_ \_ scalabilità delle porte

L'opzione socket **\_ \_ scalabilità porta** è in grado di abilitare la scalabilità delle porte locali per un socket.

<dl> <dt>

<span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**\_ \_ scalabilità delle porte**
</dt> <dd> <dl> <dt>

0x3006
</dt> <dt>



L'opzione per il socket di **\_ \_ scalabilità** delle porte consente la scalabilità della porta locale consentendo l'ingrandimento dell'allocazione delle porte allocando più volte le porte con caratteri jolly per diverse coppie di porte di indirizzi locali in un computer locale


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nota: sulle piattaforme in cui \_ \_ sono supportate sia la scalabilità delle porte che quindi il \_ riutilizzo \_ di UNICASTPORT, è preferibile usare questo \_ \_ UNICASTPORT.

Gli ambienti del server proxy presentano problemi di scalabilità a causa della disponibilità limitata delle porte locali. Un modo per risolvere questo problema consiste nell'aggiungere altri indirizzi IP al computer. Tuttavia, per impostazione predefinita, le porte con caratteri jolly usati con la funzione di [**Binding**](/windows/desktop/api/winsock/nf-winsock-bind) sono limitate alla dimensione dell'intervallo di porte dinamiche nel computer locale (fino alle porte 64K, ma in genere meno) indipendentemente dal numero di indirizzi IP nel computer locale. Per risolvere questo problema, è necessario che l'applicazione mantenga il proprio pool di porte con la prenotazione delle porte o con l'euristica.

Per evitare che tutte le applicazioni che richiedono la scalabilità gestiscano il proprio pool di porte e che consentano una maggiore scalabilità mantenendo la compatibilità delle applicazioni, in Windows Server 2008 è stata introdotta l'opzione per il socket di **\_ \_ scalabilità** delle porte che consente di ottimizzare l'allocazione L'allocazione delle porte viene ottimizzata consentendo a un'applicazione di allocare le porte con caratteri jolly per ogni coppia di porte e indirizzi locali univoci. Quindi, se un computer locale dispone di quattro indirizzi IP, è possibile allocare fino a 256 K porte con caratteri jolly (64 K porte × 4 indirizzi IP) tramite le richieste di funzioni di [**Binding**](/windows/desktop/api/winsock/nf-winsock-bind) con caratteri jolly.

Quando l'opzione socket **\_ \_ scalabilità porta** è impostata su un socket e viene eseguita una chiamata alla funzione [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) per un indirizzo specificato e una porta con caratteri jolly (il parametro *Name* è impostato con un indirizzo specifico e una porta 0), Winsock alloca una porta per l'indirizzo specificato. Questa allocazione sarà basata su tutti i possibili indirizzi IP e porte/per indirizzo nel computer locale. Se una porta con caratteri jolly viene acquisita utilizzando l'opzione **per la \_ \_ scalabilità della porta** , tale porta non può essere allocata da un altro socket senza l'opzione di **\_ \_ scalabilità delle porte** . Questa restrizione è prevista per evitare problemi di compatibilità con le applicazioni che presuppongono una porta locale con caratteri jolly non può essere riutilizzata. Si noti che questo significa che le applicazioni che acquisiscono un numero elevato di porte usando **così la \_ \_ scalabilità** delle porte possono decarere le applicazioni legacy delle porte. Se tutte le porte temporanee disponibili sono state acquisite per almeno un indirizzo con la **\_ \_ scalabilità della porta** , non è possibile allocare più porte con caratteri jolly senza l'opzione socket.

Per avere un effetto, è necessario impostare l'opzione per la **\_ \_ scalabilità della porta** , prima di chiamare la funzione di [**associazione**](/windows/desktop/api/winsock/nf-winsock-bind) . Di seguito è riportato un esempio di come verrà usato in un computer con due indirizzi:

-   La funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) viene chiamata da un processo per creare un socket.
-   La funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) viene chiamata per abilitare l'opzione socket di **\_ \_ scalabilità delle porte** nel socket appena creato.
-   La funzione [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) viene chiamata per eseguire un'associazione su uno degli indirizzi IP del computer locale e sulla porta 0.
-   La funzione [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) viene quindi chiamata per connettersi a un indirizzo IP remoto. Il socket viene usato dall'applicazione in base alle esigenze.
-   Una funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) viene chiamata dallo stesso processo (possibilmente un thread diverso) per creare un secondo socket.
-   La funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) viene chiamata per abilitare l'opzione socket di **\_ \_ scalabilità delle porte** nel secondo socket appena creato.
-   La funzione [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) viene chiamata con il secondo indirizzo IP del computer locale e la porta 0. Anche quando tutte le porte sono state allocate in precedenza, la chiamata ha esito positivo perché nel computer locale sono disponibili più indirizzi IP e l'opzione per il socket di **\_ \_ scalabilità della porta** è stata impostata su entrambi i socket nello stesso processo.
-   La funzione [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) viene quindi chiamata per connettersi a un indirizzo IP remoto. Il secondo socket viene usato dall'applicazione in base alle esigenze.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Ws2def. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**\_Opzioni Socket socket Sol**](sol-socket-socket-options.md)
</dt> <dt>

[**Opzioni socket**](socket-options.md)
</dt> </dl>

 

 




