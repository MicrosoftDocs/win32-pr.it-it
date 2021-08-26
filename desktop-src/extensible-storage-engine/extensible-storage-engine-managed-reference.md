---
description: 'Altre informazioni su: Extensible Archiviazione Engine Managed Reference'
title: Riferimento gestito del motore Archiviazione extensible
TOCTitle: Extensible Storage Engine Managed Reference
ms:assetid: b6dc69d0-82be-478d-b47f-37d7569cd200
ms:mtpsurl: https://msdn.microsoft.com/library/Dn375980(v=EXCHG.10)
ms:contentKeyID: 56355772
ms.date: 09/02/2015
ms.topic: article
ms.openlocfilehash: 38f7f09d441fa6f4158594caa8eda0b15bbe07fe909a73cd194f0886bb29914d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120093681"
---
# <a name="extensible-storage-engine-managed-reference"></a>Riferimento gestito del motore Archiviazione extensible

Trovare informazioni di riferimento per la libreria ManagedESENT. La libreria ManagedESENT fornisce l'accesso gestito a ESENT, il motore di database incorporabile nativo per Windows.


_**Si applica a:** Windows | Windows Server_

**In questo articolo**  
In che modo la libreria ManagedESENT è diversa da ESENT?  
Requisiti  
Contenuto della sezione  

## <a name="how-is-the-managedesent-library-different-than-esent"></a>In che modo la libreria ManagedESENT è diversa da ESENT?

ESENT è un motore di database transazionale incorporabile che consente di creare applicazioni personalizzate che necessitano di un'archiviazione affidabile, ad alte prestazioni e a basso sovraccarico dei dati. Il motore ESENT può essere utile per le esigenze di dati che vanno da un elemento semplice come una tabella hash troppo grande per archiviare in memoria, a qualcosa di più complesso, ad esempio un'applicazione con tabelle, colonne e indici. Per creare un'applicazione con ESENT, usare la DLL esent.dll che fa parte del sistema operativo Windows e scrivere il codice con C/C++. Per altre informazioni su ESENT, vedere [Extensible Archiviazione Engine Reference](./extensible-storage-engine-reference.md).

ManagedESENT è basato su esent.dll, che fa parte di Windows, quindi non sono presenti file binari non gestiti aggiuntivi da scaricare e installare. Con la libreria ManagedESENT è possibile creare l'applicazione usando un linguaggio gestito come C \# anziché C/C++. La libreria usa gli stessi nomi di tipo e membro per esporre l'API ESE, quindi se si ha già familiarità con la struttura di questa API, è possibile passare facilmente a questa libreria gestita.

## <a name="requirements"></a>Requisiti

Questa libreria gestita richiede quanto segue:

  - Un computer che esegue una versione di Windows a partire da Windows Vista

  - Visual Studio 2012

  - .NET Framework 4.5

## <a name="in-this-section"></a>Contenuto della sezione

  - [Microsoft.Isam.Esent](./microsoft.isam.esent-namespace.md)

  - [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

  - [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)

  - [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)

  - [Microsoft.Isam.Esent.Interop.Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)

  - [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
