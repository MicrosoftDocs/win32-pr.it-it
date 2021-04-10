---
description: Parametri dei supporti
ms.assetid: 48b2bc2e-897d-4aa9-8a50-c2855a17dca5
title: Parametri dei supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9276a3d38b9176458299bfd1a47057cac6236e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103885964"
---
# <a name="media-parameters"></a>Parametri dei supporti

I parametri multimediali consentono a un'applicazione di configurare le proprietà di un oggetto in modo che cambino nel tempo in modo matematico.

Si supponga, ad esempio, che un ingegnere del suono stia combinando un nastro master digitale e voglia applicare un lieve ritardo a una sezione vocale per compilare il suono. L'effetto sarà stridente se il ritardo si interrompe bruscamente. Al contrario, l'effetto dovrebbe iniziare il 100% a secco (nessun ritardo) e la combinazione Wet/Dry dovrebbe aumentare gradualmente fino a raggiungere il livello desiderato. Questa transizione dovrebbe inoltre seguire una curva uniforme o una progressione lineare. Per supportare questo scenario, un DMO può esporre le interfacce seguenti:

-   [**IMediaParamInfo**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) contiene metodi per l'individuazione delle informazioni sulle proprietà supportate. In genere, il client chiamerà questi metodi prima di iniziare a trasmettere i dati.
-   [**IMediaParams**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) contengono metodi per l'impostazione delle curve che seguiranno un parametro durante il flusso.

Queste interfacce sono progettate principalmente per DMOs, ma qualsiasi oggetto può supportarle. In questa sezione il termine *parametro* si riferisce a qualsiasi proprietà che supporta queste due interfacce.

Questa sezione contiene i seguenti argomenti:

-   [Curve parametro](parameter-curves.md)
-   [Informazioni sui parametri](parameter-information.md)
-   [Segmenti busta](envelope-segments.md)
-   [Calcolo dei valori dei parametri](calculating-parameter-values.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti multimediali DirectX](directx-media-objects.md)
</dt> </dl>

 

 



