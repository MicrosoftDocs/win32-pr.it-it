---
description: Sequenza temporale
ms.assetid: 6cc36034-224c-4126-873b-0cfeceec9781
title: Sequenza temporale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d1f802f12df6ca3469b8283bd4fe8b27e22412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319540"
---
# <a name="timeline"></a>Sequenza temporale

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L'oggetto sequenza temporale gestisce tutti gli oggetti in un progetto di modifica video. Per creare questo oggetto, chiamare **CoCreateInstance**. L'identificatore di classe è CLSID \_ AMTimeline.

Per leggere i file di Windows Media™, l'applicazione deve fornire un certificato software, detto anche chiave. Registrare l'applicazione come provider di chiavi tramite l'interfaccia **IObjectWithSite** della sequenza temporale. Per ulteriori informazioni, vedere [sblocco di Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).

L'oggetto sequenza temporale espone le interfacce seguenti:

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   [**IAMTimeline**](iamtimeline.md)
-   **IObjectWithSite**
-   **IPersistStream**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello di sequenza temporale](the-timeline-model.md)
</dt> <dt>

[Creazione di una sequenza temporale](constructing-a-timeline.md)
</dt> </dl>

 

 



