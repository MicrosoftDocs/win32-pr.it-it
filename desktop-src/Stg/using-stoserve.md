---
title: Uso di StoServe
description: StoServe è una DLL destinata principalmente a essere un server COM.
ms.assetid: 32cb284a-de78-4953-9d8e-5bb87d6d5a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3a220f03e17892b02a94c1e76bafc4a869c0922973c7277589627d233175a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034751"
---
# <a name="using-stoserve"></a>Uso di StoServe

**StoServe** è una DLL progettata principalmente come server COM. Anche se può essere caricato in modo implicito collegando all'oggetto associato. LIB, viene in genere usato dopo una chiamata esplicita a LoadLibrary, in genere dall'interno della funzione COM [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject). **StoServe** è un server in-process autoregistrato.

Per usare **StoServe,** non è necessario che un programma client includa STOSERVE. H o collegamento a STOSERVE. Lib. Un client COM di **StoServe** ottiene l'accesso esclusivamente tramite il CLSID e i servizi COM del relativo oggetto. Per **StoServe**, tale CLSID è CLSID \_ DllPaper (definito nel file PAPGUIDS. H nella \\ directory inc di pari livello). [L'esempio di codice StoClien](structured-storage-client-sample--stoclien-.md) mostra come il client ottiene questo accesso.

Il makefile che compila questo esempio registra automaticamente il server nel Registro di sistema. È possibile avviare manualmente la registrazione automatica emettendo il comando seguente al prompt dei comandi nella directory **StoServe:**

**Registro nmake** 

Si presuppone che sia configurato un ambiente di compilazione. In caso contrario, è anche possibile richiamare direttamente REGISTER.EXE comando al prompt dei comandi nella directory **StoServe.**

**..\\ registrare \\register.exe** **stoserve.dll**

Questi comandi di registrazione richiedono una build precedente dell'esempio REGISTER in questa serie, nonché una build precedente di STOSERVE.DLL.

In questa serie i makefile usano l'REGISTER.EXE dell'esempio REGISTER. Le versioni recenti di Platform Software Development Kit (SDK) e Visual C++ includono un'utilità, REGSVR32.EXE, che può essere usata in modo simile per registrare server in-process e effettuare il marshalling delle DLL.

**StoServe** usa molte delle classi di utilità e dei servizi forniti da APPUTIL. Per altre informazioni su APPUTIL, vedere il codice sorgente della libreria APPUTIL nella directory APPUTIL di pari livello e APPUTIL.HTM nella directory principale dell'esercitazione.

 

 