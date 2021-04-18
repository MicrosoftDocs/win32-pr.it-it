---
title: Uso di StoServe
description: StoServe è una DLL destinata principalmente a un server COM.
ms.assetid: 32cb284a-de78-4953-9d8e-5bb87d6d5a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d46dfd4070e9951223e0a498184b8db814c7a43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300206"
---
# <a name="using-stoserve"></a>Uso di StoServe

**StoServe** è una dll destinata principalmente a un server com. Sebbene possa essere caricato in modo implicito tramite il collegamento al relativo oggetto associato. Il file LIB viene in genere usato dopo una chiamata LoadLibrary esplicita, in genere dalla funzione COM [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject). **StoServe** è un server in-process con registrazione automatica.

Per usare **StoServe**, non è necessario che un programma client includa StoServe. H o collegamento a STOSERVE. LIB. Un client COM di **StoServe** Ottiene l'accesso esclusivamente tramite il CLSID e i servizi com dell'oggetto. Per **StoServe**, il CLSID è CLSID \_ DllPaper (definito nel file PAPGUIDS. H nella \\ directory di pari livello Inc. L'esempio di codice [StoClien](structured-storage-client-sample--stoclien-.md) Mostra come il client ottiene questo accesso.

Il makefile che compila questo esempio registra automaticamente il server nel registro di sistema. È possibile avviare manualmente la registrazione automatica eseguendo il comando seguente al prompt dei comandi nella directory **StoServe** :

 **Registro** NMAKE

Si presuppone che sia configurato un ambiente di compilazione. In caso contrario, è anche possibile richiamare direttamente il REGISTER.EXE comando al prompt dei comandi, mentre si trovi nella directory **StoServe**

**..\\ Registra \\register.exe** **stoserve.dll**

Questi comandi di registrazione richiedono una compilazione precedente dell'esempio di registrazione in questa serie, oltre a una build precedente di STOSERVE.DLL.

In questa serie i makefile usano l'utilità REGISTER.EXE dall'esempio REGISTER. Le versioni recenti di Platform Software Development Kit (SDK) e Visual C++ includono un'utilità, REGSVR32.EXE, che può essere usata in modo analogo per registrare i server in-process e il marshalling delle dll.

**StoServe** usa molte delle classi e dei servizi di utilità forniti da APPUTIL. Per altri dettagli su APPUTIL, studiare il codice sorgente della libreria APPUTIL nella directory di pari livello APPUTIL e APPUTIL.HTM nella directory principale dell'esercitazione.

 

 