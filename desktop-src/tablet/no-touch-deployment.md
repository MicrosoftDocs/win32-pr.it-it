---
description: Il Framework Microsoft .NET offre la possibilità di distribuire applicazioni da un Web o file server.
ms.assetid: 7721cd92-241f-4409-a724-c8e8768a19a9
title: Nessuna distribuzione touch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6567edf35dbd79256bed228de3941351bd5e7642
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320392"
---
# <a name="no-touch-deployment"></a>Nessuna distribuzione touch

Il Framework Microsoft .NET offre la possibilità di distribuire applicazioni da un Web o file server. Questa tecnica, denominata "distribuzione senza tocco", combina le prestazioni e l'interattività di un'applicazione smart client con tutti i vantaggi della distribuzione di un'applicazione Web. Per distribuire l'applicazione sul Web, fare clic con il pulsante destro del mouse sulla cartella che contiene il file eseguibile e scegliere **Proprietà**. Nella scheda **condivisione Web** selezionare **Condividi questa cartella**. Immettere un alias per la cartella. A questo punto, il file eseguibile può essere eseguito sul Web usando tale alias come directory nel server. Per ulteriori informazioni sulla distribuzione senza tocco, vedere la pagina relativa alla distribuzione di [smart client](/archive/msdn-magazine/2002/july/net-zero-deployment-security-and-versioning-models-in-the-windows-forms-engine-help-you-create-and-deploy-smart-clients) e [senza tocco di .NET nel .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp).

> [!Note]  
> Per abilitare la scheda **condivisione Web** nella finestra di dialogo **Proprietà** , è necessario che nel computer sia installato Microsoft Internet Information Services (IIS).

 

La distribuzione senza tocco viene applicata alle applicazioni abilitate per l'input penna in modo analogo a qualsiasi altra Windows Forms Application. Gli esempi forniti da Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) includono una versione di distribuzione senza tocco dell'esempio auto Claims, nella sezione relativa agli esempi di Web Ink degli esempi. Questo esempio illustra l'esempio originale del [modulo delle attestazioni automatiche](auto-claims-form-sample.md) e fornisce un programma di installazione che inserisce in una condivisione Web. Quando Microsoft Internet Explorer passa a AutoClaims.exe nella directory che esegue il mapping alla condivisione Web, viene avviata l'applicazione. Per ulteriori informazioni sull'esempio, vedere l'esempio di Web per la [distribuzione senza tocco](no-touch-deployment-web-sample.md) .

> [!Note]  
> Quando si distribuisce un'applicazione .NET sul Web, l'applicazione potrebbe essere interessata dal modello di sicurezza .NET. La sezione [Security and Trust](security-and-trust.md) illustra il funzionamento della sicurezza con le applicazioni Web abilitate per l'input penna.

 

 

 