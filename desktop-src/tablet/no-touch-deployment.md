---
description: Microsoft .NET Framework offre la possibilità di distribuire applicazioni da un Web o da file server.
ms.assetid: 7721cd92-241f-4409-a724-c8e8768a19a9
title: Nessuna distribuzione touch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d31f01742a1b1231171688ea15634913c56ef613c8f6ebdaf3042b4998f00a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856540"
---
# <a name="no-touch-deployment"></a>Nessuna distribuzione touch

Microsoft .NET Framework offre la possibilità di distribuire applicazioni da un Web o da file server. Questa tecnica, denominata "distribuzione senza tocco", combina le prestazioni e l'interattività di un'applicazione smart client con tutti i vantaggi di distribuzione di un'applicazione Web. Per distribuire l'applicazione sul Web, fare clic con il pulsante destro del mouse sulla cartella contenente l'eseguibile e scegliere **Proprietà**. Nella scheda **Condivisione Web** selezionare Condividi **questa cartella**. Immettere un alias per la cartella. A questo punto, l'eseguibile può essere eseguito sul Web usando tale alias come directory nel server. Per altre informazioni sulla distribuzione senza tocco, vedere [.NET Smart Clients](/archive/msdn-magazine/2002/july/net-zero-deployment-security-and-versioning-models-in-the-windows-forms-engine-help-you-create-and-deploy-smart-clients) and [No-Touch Deployment in .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp).

> [!Note]  
> È necessario aver Microsoft Internet Information Services (IIS) nel computer per abilitare la **scheda Condivisione Web** nella finestra di **dialogo** Proprietà .

 

La distribuzione senza tocco viene applicata alle applicazioni abilitate per l'input penna come qualsiasi altra applicazione Windows Forms. Gli esempi forniti da Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) includono una versione di distribuzione senza tocco dell'esempio di attestazioni automatica, nella sezione Ink Web Samples degli esempi. Questo esempio accetta l'esempio [originale di modulo attestazioni](auto-claims-form-sample.md) automatico e fornisce un programma di installazione che inserisce in una condivisione Web. Quando Microsoft Internet Explorer passa a AutoClaims.exe nella directory che esegue il mapping alla condivisione Web, viene avviata l'applicazione. Per [altre informazioni sull'esempio,](no-touch-deployment-web-sample.md) vedere Esempio Web di distribuzione no-touch.

> [!Note]  
> Quando si distribuisce un'applicazione .NET sul Web, l'applicazione potrebbe essere interessata dal modello di sicurezza .NET. La [sezione Sicurezza e attendibilità](security-and-trust.md) descrive il funzionamento della sicurezza con le applicazioni Web abilitate per l'input penna.

 

 

 