---
description: Questo esempio illustra come distribuire un'applicazione Tablet PC gestita sul Web usando una distribuzione senza tocco.
ms.assetid: d226bd67-e20d-431b-b0c3-9361b00a9340
title: No-Touch Web di distribuzione di applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d8fb9989785dc081022c2e76d8fade6d48bf521b3f27449ff5aac963706f356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449652"
---
# <a name="no-touch-deployment-web-sample"></a>No-Touch Web di distribuzione di applicazioni

Questo esempio illustra come distribuire un'applicazione Tablet PC gestita sul Web usando una distribuzione senza tocco. È necessario avere familiarità con i concetti illustrati in [No-Touch Deployment (Distribuzione senza tocco) .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp). Per eseguire questo esempio, nel computer deve essere installato Microsoft Internet Information Services (IIS).

## <a name="overview"></a>Panoramica

Con la distribuzione senza tocco, Tablet PCWindows Forms applications-desktop applications built by using the classes in the System. Windows. Lo spazio dei nomi Forms di Microsoft .NET Framework e Microsoft Windows XP Tablet PC Edition Development Kit 1.7 possono essere scaricati, installati ed eseguiti direttamente nei computer degli utenti senza alcuna modifica del Registro di sistema o dei componenti di sistema condivisi.

Questo esempio prende il progetto originale per [Auto Claims Form Sample](auto-claims-form-sample.md), AutoClaims e fornisce un progetto di installazione, AutoClaims \_ NoTouchWeb. Dopo la compilazione e l'esecuzione, il progetto di installazione crea una nuova radice virtuale, denominata anche AutoClaims \_ NoTouchWeb. Il programma di installazione copia un file, default.htm, che include un collegamento all'assembly AutoClaims.exe. Per avviare l'applicazione rich client, passare alla radice virtuale con Microsoft Internet Explorer e quindi fare clic sul collegamento nella default.htm pagina.

> [!Note]  
> È necessario passare alla radice virtuale tramite IIS, ad esempio e non direttamente tramite il file system, perché l'applicazione funzioni nel dominio applicazione https://localhost/AutoClaims\_NoTouchWeb/default.htm) Internet Explorer.

 


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



## <a name="no-touch-deployment-requirements"></a>No-Touch di distribuzione

Tutti gli assembly dipendenti devono trovarsi nel percorso di ricerca degli assembly o nella radice della directory virtuale del sito Web. Il progetto di distribuzione AutoClaims NoTouchWeb installa l'assembly e la pagina di riferimento, default.htm, nella stessa radice virtuale \_ (AutoClaims \_ NoTouchWeb).

> [!Note]  
> Gli esempi Web compilati non vengono installati dall'opzione di installazione predefinita per l'SDK. È necessario completare un'installazione personalizzata e selezionare l'opzione secondaria "Pre-compiled Web Samples" (Esempi Web precompilato) per installarli.

 

Per altre informazioni sull'uso dell'input penna sul Web, [vedere Ink on the Web (Input penna sul Web).](ink-on-the-web.md)

 

 