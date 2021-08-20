---
title: Per sospendere o arrestare la riproduzione
description: Per sospendere o arrestare la riproduzione
ms.assetid: 8e43ea80-36c7-4530-8ed3-dfdb64a3a2e3
keywords:
- Advanced Systems Format (ASF), sospensione della riproduzione
- ASF (Advanced Systems Format), sospensione della riproduzione
- Advanced Systems Format (ASF), lettori asincroni
- ASF (Advanced Systems Format),lettori asincroni
- Advanced Systems Format (ASF), arresto della riproduzione
- ASF (Advanced Systems Format), arresto della riproduzione
- Advanced Systems Format (ASF), riproduzione in pausa o arresto
- ASF (Advanced Systems Format), riproduzione in pausa o arresto
- lettori asincroni, sospensione della riproduzione
- lettori asincroni, arresto della riproduzione
- lettori asincroni, riproduzione in pausa o arresto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7ae7f3c1dd2c045a35b8d3ee8950ace849a032136371f9da7ff1bcc2b12de27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845366"
---
# <a name="to-pause-or-stop-playback"></a>Per sospendere o arrestare la riproduzione

Quando si chiama [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) per avviare la riproduzione di un file, il lettore asincrono continuerà l'elaborazione nei propri thread separati fino a quando non viene raggiunta la fine del file. È possibile sospendere o arrestare il recapito degli esempi usando rispettivamente i metodi [**IWMReader::P ause**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) o [**IWMReader::Stop.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop)

## <a name="pausing"></a>Sospensione

Quando si chiama **IWMReader::P ause** per sospendere la riproduzione di un file, il lettore tiene traccia della posizione corrente nel file. Per riprendere la riproduzione dopo la sospensione, chiamare [**IWMReader::Resume**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume). La riproduzione riprenderà dal punto in cui è stata sospesa.

## <a name="stopping"></a>Stopping

Quando si chiama **IWMReader::Stop** per interrompere la riproduzione di un file, il lettore non tiene traccia delle informazioni sullo stato di avanzamento della riproduzione. Per usare **Stop** e tornare successivamente al punto di arresto, è necessario salvare l'ora di presentazione dell'ultimo esempio recapitato e usarlo nella chiamata a **IWMReader::Start**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Lettura di file con il lettore asincrono**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




