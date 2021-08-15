---
description: Abilita la scalabilità delle porte locali per un socket.
ms.assetid: c5142baf-9e2d-4c06-8719-9090fd2d9487
title: SO_PORT_SCALABILITY (Ws2def.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 925d6337bc5b9d4633117fc1d8e1b8db2657f31b91a9cce602702ceb67e7e92e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993371"
---
# <a name="so_port_scalability"></a>SCALABILITÀ \_ \_ DELLE PORTE

**L'opzione socket SO PORT \_ \_ SCALABILITY** consente la scalabilità delle porte locali per un socket.

<dl> <dt>

<span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**SCALABILITÀ \_ \_ DELLE PORTE**
</dt> <dd> <dl> <dt>

0x3006
</dt> <dt>



**L'opzione socket SO PORT \_ \_ SCALABILITY** consente la scalabilità delle porte locali consentendo di ottimizzare l'allocazione delle porte allocando più volte porte con caratteri jolly per diverse coppie di porte di indirizzi locali in un computer locale.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nota: nelle piattaforme in cui sono supportati SIA SO PORT SCALABILITY che SO REUSE UNICASTPORT, è preferibile usare \_ \_ SO REUSE \_ \_ \_ \_ UNICASTPORT.

Gli ambienti server proxy hanno problemi di scalabilità a causa della disponibilità limitata delle porte locali. Un modo per risolvere questo problema è aggiungere altri indirizzi IP al computer. Tuttavia, per impostazione predefinita, le porte con caratteri jolly usate con la funzione [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) sono limitate alle dimensioni dell'intervallo di porte dinamiche nel computer locale (fino a 64.000 porte, ma in genere meno) indipendentemente dal numero di indirizzi IP nel computer locale. Per risolvere questo problema, è necessario che l'applicazione mantenga il proprio pool di porte con prenotazione di porte o usando l'euristica.

Per evitare che ogni applicazione che richiede scalabilità gestisse il proprio pool di porte e consentire una maggiore scalabilità mantenendo la compatibilità delle applicazioni, Windows Server 2008 ha introdotto l'opzione socket **SO \_ PORT \_ SCALABILITY** per ottimizzare l'allocazione delle porte con caratteri jolly. L'allocazione delle porte viene ottimizzata consentendo a un'applicazione di allocare porte con caratteri jolly per ogni coppia di porte e indirizzi locali univoci. Pertanto, se un computer locale ha quattro indirizzi IP, è possibile allocare fino a 256.000 [](/windows/desktop/api/winsock/nf-winsock-bind) porte jolly (64.000 porte × 4 indirizzi IP) dalle richieste di funzione di associazione con caratteri jolly.

Quando l'opzione socket **SO PORT \_ \_ SCALABILITY** è impostata su un socket e viene effettuata una chiamata alla funzione di associazione per un indirizzo e una porta jolly specificati (il parametro *name* è impostato con un indirizzo specifico e una porta 0), Winsock alloca una porta per l'indirizzo specificato. [](/windows/desktop/api/winsock/nf-winsock-bind) Questa allocazione sarà basata su tutti i possibili indirizzi IP e porte/per indirizzo nel computer locale. Se una porta con caratteri jolly viene acquisita usando l'opzione **SO \_ PORT \_ SCALABILITY,** tale porta non può essere allocata da un altro socket senza l'opzione **SO PORT \_ \_ SCALABILITY.** Questa restrizione è stata impostata per evitare problemi di compatibilità con le versioni precedenti delle applicazioni che presuppongono che non sia possibile riutilizzare una porta locale con caratteri jolly. Si noti che ciò significa che le applicazioni che acquisiscono un numero elevato di porte usando **SO \_ PORT \_ SCALABILITY** possono affamare le applicazioni legacy delle porte. Se sono state acquisite tutte le porte provvisorie disponibili per almeno un indirizzo con **SO \_ PORT \_ SCALABILITY,** non sono possibili altre allocazioni di porte con caratteri jolly senza l'opzione socket.

Per ottenere qualsiasi effetto, è necessario impostare **l'opzione SO \_ PORT \_ SCALABILITY** prima che venga [**chiamata**](/windows/desktop/api/winsock/nf-winsock-bind) la funzione di associazione. Di seguito è riportato un esempio di come verrà usato in un computer con due indirizzi:

-   La [**funzione socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) viene chiamata da un processo per creare un socket.
-   La [**funzione setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) viene chiamata per abilitare l'opzione **socket SO PORT \_ \_ SCALABILITY** nel socket appena creato.
-   La [**funzione**](/windows/desktop/api/winsock/nf-winsock-bind) bind viene chiamata per eseguire un'associazione su uno degli indirizzi IP del computer locale e sulla porta 0.
-   La [**funzione connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) viene quindi chiamata per connettersi a un indirizzo IP remoto. Il socket viene usato dall'applicazione in base alle esigenze.
-   Una [**funzione socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) viene chiamata dallo stesso processo (possibilmente un thread diverso) per creare un secondo socket.
-   La [**funzione setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) viene chiamata per abilitare l'opzione **socket SO PORT \_ \_ SCALABILITY** nel secondo socket appena creato.
-   La [**funzione**](/windows/desktop/api/winsock/nf-winsock-bind) bind viene chiamata con il secondo indirizzo IP del computer locale e la porta 0. Anche quando tutte le porte sono state allocate in precedenza, questa chiamata ha esito positivo perché sono disponibili più indirizzi IP nel computer locale ed è stata impostata l'opzione socket **SO \_ PORT \_ SCALABILITY** su entrambi i socket nello stesso processo.
-   La [**funzione connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) viene quindi chiamata per connettersi a un indirizzo IP remoto. Il secondo socket viene usato dall'applicazione in base alle esigenze.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Ws2def.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**Setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**Opzioni socket SOCKET SOL \_**](sol-socket-socket-options.md)
</dt> <dt>

[**Opzioni socket**](socket-options.md)
</dt> </dl>

 

 




