---
description: In questa sezione vengono descritte le considerazioni sul porting Winsock.
ms.assetid: 41c0c98e-3990-4600-ab9f-fa87edbea402
title: Porting delle applicazioni socket in Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2b3480d5572405d33b3a3532892a48633caa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306908"
---
# <a name="porting-socket-applications-to-winsock"></a>Porting delle applicazioni socket in Winsock

In questa sezione vengono descritte le considerazioni sul porting Winsock.

Il numero di istanze di Windows Sockets è limitato da una stretta aderenza alle convenzioni di Berkeley, in genere a causa di problemi di implementazione nell'ambiente Microsoft Windows.

Quando si verifica una deviazione dalle convenzioni di Berkeley in Windows Sockets, la deviazione è specifica e chiaramente nota. Ad esempio, se una funzione è specifica di Windows Sockets, tale deviazione viene specificata con una frase nella descrizione della funzione simile alla seguente:

La funzione del **\[ nome \] di funzione** è un'estensione specifica di Microsoft per l'API di Windows Sockets 2.

In questa sezione vengono fornite informazioni sul porting delle applicazioni socket UNIX di Berkeley (BSD) a Winsock:

-   [Tipo di dati socket](socket-data-type-2.md)
-   [Macro Select, FD \_ set e FD \_ xxx](select-and-fd---2.md)
-   [Codici di errore-errno, h \_ errno e WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
-   [Pointers](pointers-2.md)
-   [Funzioni rinominate](renamed-functions-2.md)
-   [Numero massimo di socket supportati](maximum-number-of-sockets-supported-2.md)
-   [File di inclusione](include-files-2.md)
-   [Valori restituiti sull'errore della funzione](return-values-on-function-failure-2.md)
-   [Socket non elaborati](service-provided-raw-sockets-2.md)
-   [Ordinamento byte](byte-ordering-2.md)
-   [Routine di conversione Byte-Order estese](extended-byte-order-conversion-routines-2.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione degli errori Winsock](handling-winsock-errors.md)
</dt> <dt>

[Porting delle applicazioni socket in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Codici di errore di Windows Sockets](windows-sockets-error-codes-2.md)
</dt> <dt>

[Considerazioni sulla programmazione Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



