---
description: 'Altre informazioni su: riferimento gestito del motore di archiviazione estendibile'
title: Riferimento gestito del motore di archiviazione estendibile
TOCTitle: Extensible Storage Engine Managed Reference
ms:assetid: b6dc69d0-82be-478d-b47f-37d7569cd200
ms:mtpsurl: https://msdn.microsoft.com/library/Dn375980(v=EXCHG.10)
ms:contentKeyID: 56355772
ms.date: 09/02/2015
ms.topic: article
ms.openlocfilehash: a1323d662cc7252ff6bda1eda53108751d3aedfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049672"
---
# <a name="extensible-storage-engine-managed-reference"></a>Riferimento gestito del motore di archiviazione estendibile

Trovare le informazioni di riferimento per la libreria ManagedESENT. La libreria ManagedESENT fornisce l'accesso gestito a ESENT, il motore di database incorporabile nativo di Windows.


_**Si applica a:** Windows | Windows Server_

**In questo articolo**  
In che modo la libreria ManagedESENT è diversa da ESENT?  
Requisiti  
Contenuto della sezione  

## <a name="how-is-the-managedesent-library-different-than-esent"></a>In che modo la libreria ManagedESENT è diversa da ESENT?

ESENT è un motore di database transazionale incorporabile che consente di creare applicazioni personalizzate che richiedono un'archiviazione dei dati affidabile, a prestazioni elevate e con sovraccarico ridotto. Il motore ESENT può aiutare a soddisfare le esigenze dei dati che variano da qualcosa di semplice come una tabella hash troppo grande per l'archiviazione in memoria, in un elemento più complesso, ad esempio un'applicazione con tabelle, colonne e indici. Per creare un'applicazione con ESENT, è possibile usare la DLL esent.dll che fa parte del sistema operativo Windows e scrivere il codice con C/C++. Per altre informazioni su ESENT, vedere informazioni di [riferimento sul motore di archiviazione estensibile](./extensible-storage-engine-reference.md).

ManagedESENT si basa su esent.dll, che fa parte di Windows, quindi non sono presenti file binari non gestiti aggiuntivi da scaricare e installare. Con la libreria ManagedESENT è possibile creare l'applicazione usando un linguaggio gestito, ad esempio C \# anziché c/C++. La libreria usa lo stesso tipo e i nomi di membro per esporre l'API ESE, quindi se si ha già familiarità con la struttura di questa API, è possibile passare facilmente a questa libreria gestita.

## <a name="requirements"></a>Requisiti

Questa libreria gestita richiede gli elementi seguenti:

  - Un computer che esegue una versione di Windows a partire da Windows Vista

  - Visual Studio 2012

  - .NET Framework 4.5

## <a name="in-this-section"></a>Contenuto della sezione

  - [Microsoft. ISAM. ESENT](./microsoft.isam.esent-namespace.md)

  - [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

  - [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)

  - [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)

  - [Microsoft. ISAM. esent. Interop. Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)

  - [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
