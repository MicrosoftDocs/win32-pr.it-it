---
description: In questo esempio viene illustrato come distribuire un'applicazione Tablet PC gestita sul Web utilizzando la distribuzione senza tocco.
ms.assetid: d226bd67-e20d-431b-b0c3-9361b00a9340
title: Esempio di Web Deployment No-Touch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0742deef8ea9b418fba6de4724975ee27693f8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104530444"
---
# <a name="no-touch-deployment-web-sample"></a>Esempio di Web Deployment No-Touch

In questo esempio viene illustrato come distribuire un'applicazione Tablet PC gestita sul Web utilizzando la distribuzione senza tocco. È necessario avere familiarità con i concetti illustrati nella [distribuzione senza tocco nella .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp). Per eseguire l'esempio, è necessario che nel computer sia installato Microsoft Internet Information Services (IIS).

## <a name="overview"></a>Panoramica

Con la distribuzione senza tocco, le applicazioni tablet PCWindows Forms-applicazioni desktop compilate usando le classi nello spazio dei nomi System. Windows. Forms di Microsoft .NET Framework e Microsoft Windows XP Tablet PC Edition Development Kit 1,7-possono essere scaricate, installate ed eseguite direttamente sui computer degli utenti senza alcuna modifica del registro di sistema o dei componenti di sistema condivisi.

Questo esempio accetta il progetto originale per l' [esempio di modulo delle attestazioni automatiche](auto-claims-form-sample.md), autoclaims e fornisce un progetto di programma di installazione, autoclaims \_ NoTouchWeb. Una volta compilata ed eseguita, il progetto di installazione crea una nuova radice virtuale, denominata anche autoclaims \_ NoTouchWeb. Il programma di installazione copia un file, default.htm, che include un collegamento all'assembly AutoClaims.exe. Per avviare l'applicazione rich client, passare alla radice virtuale con Microsoft Internet Explorer, quindi fare clic sul collegamento nella pagina default.htm.

> [!Note]  
> È necessario passare alla radice virtuale tramite IIS (ad esempio, https://localhost/AutoClaims\_NoTouchWeb/default.htm) e non direttamente tramite il file System per consentire l'uso dell'applicazione nel dominio applicazione di Internet Explorer.

 


```C++
<html>
    <head>
        <title>AutoClaims (No Touch Web)</title>
      </head>
      <body>
          <a href="AutoClaims.exe">Launch AutoClaims Sample</a>
      </body>
</html>
```



## <a name="no-touch-deployment-requirements"></a>Requisiti per la distribuzione di No-Touch

Tutti gli assembly dipendenti devono trovarsi nel percorso di ricerca dell'assembly o nella radice della directory virtuale del sito Web. Il progetto di distribuzione autoclaims \_ NoTouchWeb installa l'assembly e la pagina di riferimento, default.htm, nella stessa radice virtuale (Autoclaims \_ NoTouchWeb).

> [!Note]  
> Gli esempi Web compilati non vengono installati tramite l'opzione di installazione predefinita per l'SDK. È necessario completare un'installazione personalizzata e selezionare l'opzione secondaria "esempi Web precompilati" per installarli.

 

Per ulteriori informazioni sull'utilizzo di input penna sul Web, vedere [input penna sul Web](ink-on-the-web.md).

 

 