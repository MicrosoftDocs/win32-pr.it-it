---
title: Per sospendere o arrestare la riproduzione
description: Per sospendere o arrestare la riproduzione
ms.assetid: 8e43ea80-36c7-4530-8ed3-dfdb64a3a2e3
keywords:
- Formato Advanced Systems (ASF), sospensione della riproduzione
- ASF (formato avanzato dei sistemi), sospensione della riproduzione
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- Formato Advanced Systems (ASF), arresto della riproduzione
- ASF (formato avanzato dei sistemi), arresto della riproduzione
- ASF (Advanced Systems Format), sospensione o arresto della riproduzione
- ASF (formato avanzato dei sistemi), sospensione o arresto della riproduzione
- lettori asincroni, sospensione della riproduzione
- lettori asincroni, arresto della riproduzione
- lettori asincroni, sospensione o arresto della riproduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728ce4c58f9198f605764d0f19d0d5f55c7f6c6b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104516597"
---
# <a name="to-pause-or-stop-playback"></a>Per sospendere o arrestare la riproduzione

Quando si chiama [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) per iniziare la riproduzione di un file, il Reader asincrono continuerà l'elaborazione nei propri thread distinti fino a quando non viene raggiunta la fine del file. È possibile sospendere o arrestare il recapito degli esempi usando rispettivamente i metodi [**IWMReader::P ause**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) o [**IWMReader:: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop) .

## <a name="pausing"></a>Sospensione

Quando si chiama **IWMReader::P ause** per sospendere la riproduzione di un file, il lettore tiene traccia della posizione corrente nel file. Per riprendere la riproduzione dopo la sospensione, chiamare [**IWMReader:: Resume**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume). La riproduzione riprenderà dal punto in cui è stata sospesa.

## <a name="stopping"></a>Stopping

Quando si chiama **IWMReader:: Stop** per interrompere la riproduzione di un file, il lettore non tiene traccia delle informazioni sullo stato di avanzamento della riproduzione. Per usare **Interrompi** e versioni successive per tornare al punto di arresto, è necessario salvare l'ora di presentazione dell'ultimo esempio recapitato e usarlo nella chiamata a **IWMReader:: Start**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Lettura di file con il lettore asincrono**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




