---
description: Parametri dei supporti
ms.assetid: 48b2bc2e-897d-4aa9-8a50-c2855a17dca5
title: Parametri dei supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37cf7229cac3deb5b31a6c6879fd3b5896e5f4098a4cce64ac42d19970f5c569
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584341"
---
# <a name="media-parameters"></a>Parametri dei supporti

I parametri multimediali consentono a un'applicazione di configurare le proprietà di un oggetto in modo che cambino nel tempo in modo matematicamente deterministico.

Si supponga, ad esempio, che un tecnico del suono voglia combinare un nastro master digitale e voglia applicare un leggero ritardo a una sezione vocale, per compilare il suono. L'effetto sarà stridente se il ritardo si riduce improvvisamente. L'effetto dovrebbe invece iniziare a secco al 100% (nessun ritardo) e la combinazione umida/asciutta dovrebbe aumentare gradualmente fino a raggiungere il livello desiderato. Inoltre, questa transizione deve seguire una curva smussato o una progressione lineare. Per supportare questo scenario, un DMO può esporre le interfacce seguenti:

-   [**IMediaParamInfo contiene**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) metodi per l'individuazione di informazioni sulle proprietà supportate. In genere, il client chiamerà questi metodi prima di iniziare a trasmettere i dati.
-   [**IMediaParams contengono**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) metodi per impostare le curve che un parametro seguirà durante lo streaming.

Queste interfacce sono progettate principalmente per le DMO, ma qualsiasi oggetto può supportarle. All'interno di questa sezione, il termine *parametro* fa riferimento a qualsiasi proprietà che supporta queste due interfacce.

Questa sezione contiene i seguenti argomenti:

-   [Curve dei parametri](parameter-curves.md)
-   [Informazioni sui parametri](parameter-information.md)
-   [Segmenti di busta](envelope-segments.md)
-   [Calcolo dei valori dei parametri](calculating-parameter-values.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti multimediali DirectX](directx-media-objects.md)
</dt> </dl>

 

 



