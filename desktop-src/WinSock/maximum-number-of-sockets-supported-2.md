---
description: Il numero massimo di socket supportati da un particolare provider di servizi Windows Sockets è specifico dell'implementazione.
ms.assetid: acf5ab29-3848-4dbc-afa7-a0f19045ddec
title: Numero massimo di socket supportati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207893836a411a2465ffcefe10e838c2e8b59011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306931"
---
# <a name="maximum-number-of-sockets-supported"></a>Numero massimo di socket supportati

Il numero massimo di socket supportati da un particolare provider di servizi Windows Sockets è specifico dell'implementazione. Il provider Microsoft Winsock limita il numero massimo di socket supportati solo dalla memoria disponibile nel computer locale. Tuttavia, i provider Winsock di terze parti possono avere limitazioni sul numero di socket supportati. Un'applicazione non deve fare supposizioni sulla disponibilità di un determinato numero di socket. Per ulteriori informazioni su questo argomento, vedere [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup).

## <a name="fd_set-and-select"></a>FD \_ impostare e selezionare

\_Nel file di intestazione *Winsock2. h* sono definite diverse macro fd XXX da usare per il porting delle applicazioni a Windows dall'ambiente UNIX. Queste macro vengono usate con le funzioni [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) e [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) per il porting delle applicazioni a Windows. Il numero massimo di socket che possono essere usati da un'applicazione Windows Sockets non è influenzato dalla costante di manifesto FD \_ sesize. Questo valore definito nel file di intestazione *Winsock2. h* viene utilizzato per la costruzione delle strutture di [**\_ set FD**](/windows/desktop/api/winsock/nf-winsock-fd_set) utilizzate con la funzione **Select** . Il valore predefinito in Winsock2. h è 64. Se un'applicazione è progettata per essere in grado di utilizzare più di 64 socket usando le funzioni **Select** e **WSAPoll** , l'implementatore deve definire il manifesto di FD per \_ ogni file di origine prima di includere il file di intestazione *Winsock2. h* . Un modo per eseguire questa operazione potrebbe consistere nell'includere la definizione all'interno delle opzioni del compilatore nel makefile. È ad esempio possibile aggiungere "-DFD \_ sesize = 128" come opzione alla riga di comando del compilatore per Microsoft C++. È necessario enfatizzare che \_ la definizione di dimensioni FD come un particolare valore non influisce sul numero effettivo di socket fornito da un provider di servizi Windows Sockets. Questo valore influiscono solo sulle \_ macro fd xxx utilizzate dalle funzioni **SELECT** e **WSAPoll** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**\_set FD**](/windows/desktop/api/winsock/nf-winsock-fd_set)
</dt> <dt>

[Porting delle applicazioni socket in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**Selezionare**](/windows/desktop/api/Winsock2/nf-winsock2-select)
</dt> <dt>

[Considerazioni sulla programmazione Winsock](winsock-programming-considerations.md)
</dt> <dt>

[**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup)
</dt> <dt>

[**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll)
</dt> </dl>

 

 
