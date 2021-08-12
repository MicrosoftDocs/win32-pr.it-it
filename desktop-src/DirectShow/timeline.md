---
description: Sequenza temporale
ms.assetid: 6cc36034-224c-4126-873b-0cfeceec9781
title: Sequenza temporale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d85809aed689d63ccdfc0b1dee1b5b792cafc9d7d0267d27e33bd7b6c1bea6cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651254"
---
# <a name="timeline"></a>Sequenza temporale

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

L'oggetto sequenza temporale gestisce tutti gli oggetti in un progetto di modifica video. Per creare questo oggetto, chiamare **CoCreateInstance**. L'identificatore di classe è CLSID \_ AMTimeline.

Per leggere Windows file ™, l'applicazione deve fornire un certificato software, denominato anche chiave. Registrare l'applicazione come provider di chiavi tramite **l'interfaccia IObjectWithSite della** sequenza temporale. Per altre informazioni, vedere [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).

L'oggetto sequenza temporale espone le interfacce seguenti:

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   [**IAMTimeline**](iamtimeline.md)
-   **IObjectWithSite**
-   **Ipersiststream**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello di sequenza temporale](the-timeline-model.md)
</dt> <dt>

[Costruzione di una sequenza temporale](constructing-a-timeline.md)
</dt> </dl>

 

 



