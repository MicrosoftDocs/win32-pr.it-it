---
description: Il numero massimo di socket supportati da un provider di servizi Windows Sockets è specifico dell'implementazione.
ms.assetid: acf5ab29-3848-4dbc-afa7-a0f19045ddec
title: Numero massimo di socket supportati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b567b9733dfb869c901ac499ca8dac66904c84bbe77d750780504acee076385f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569753"
---
# <a name="maximum-number-of-sockets-supported"></a>Numero massimo di socket supportati

Il numero massimo di socket supportati da un provider di servizi Windows Sockets è specifico dell'implementazione. Il provider Microsoft Winsock limita il numero massimo di socket supportati solo dalla memoria disponibile nel computer locale. Tuttavia, i provider Winsock di terze parti possono avere limitazioni al numero di socket supportati. Un'applicazione non deve fare supposizioni sulla disponibilità di un determinato numero di socket. Per altre informazioni su questo argomento, vedere [**WSAStartup.**](/windows/desktop/api/winsock/nf-winsock-wsastartup)

## <a name="fd_set-and-select"></a>FD \_ SET e selezionare

Nel file di intestazione \_ *Winsock2.h* sono definite diverse macro FD XXX da usare nella portabilità di applicazioni Windows dall'ambiente UNIX. Queste macro vengono usate con le [**funzioni select**](/windows/desktop/api/Winsock2/nf-winsock2-select) e [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) per la portabilità di applicazioni Windows. Il numero massimo di socket che un'Windows Sockets può usare non è influenzato dalla costante manifesto FD \_ SETSIZE. Questo valore definito nel file di intestazione *Winsock2.h* viene usato per costruire le strutture [**\_ SET FD**](/windows/desktop/api/winsock/nf-winsock-fd_set) usate con la **funzione select.** Il valore predefinito in Winsock2.h è 64. Se un'applicazione è progettata per funzionare con più di 64 socket usando le funzioni **select** e **WSAPoll,** l'implementatore deve definire il manifesto FD SETSIZE in ogni file di origine prima di includere il file di intestazione \_ *Winsock2.h.* Un modo per eseguire questa operazione può essere includere la definizione all'interno delle opzioni del compilatore nel makefile. Ad esempio, è possibile aggiungere "-DFD SETSIZE=128" come opzione alla riga di comando del compilatore \_ per Microsoft C++. È necessario sottolineare che la definizione di FD SETSIZE come valore specifico non ha alcun effetto sul numero effettivo di socket forniti da un provider di servizi \_ Windows Sockets. Questo valore influisce solo sulle macro FD \_ XXX usate dalle funzioni **select** e **WSAPoll.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**FD \_ SET**](/windows/desktop/api/winsock/nf-winsock-fd_set)
</dt> <dt>

[Porting di applicazioni socket in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**Selezionare**](/windows/desktop/api/Winsock2/nf-winsock2-select)
</dt> <dt>

[Considerazioni sulla programmazione winsock](winsock-programming-considerations.md)
</dt> <dt>

[**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup)
</dt> <dt>

[**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll)
</dt> </dl>

 

 
