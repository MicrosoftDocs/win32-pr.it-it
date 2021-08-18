---
title: Individuazione delle funzionalità del formato del dispositivo
description: Individuazione delle funzionalità del formato del dispositivo
ms.assetid: dd139816-dc8c-4e73-9a21-67287bfe6405
keywords:
- Windows Gestione dispositivi multimediali, funzionalità del dispositivo
- Gestione dispositivi, funzionalità del dispositivo
- guida per programmatori, funzionalità del dispositivo
- applicazioni desktop, funzionalità dei dispositivi
- creazione Windows applicazioni di Gestione dispositivi multimediali, funzionalità del dispositivo
- scrittura di file in dispositivi, funzionalità del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e4fc32c0980a1022f7affb225918ccf0d49e5d14c5bb7310e70e7aa4f83a62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585147"
---
# <a name="discovering-device-format-capabilities"></a>Individuazione delle funzionalità del formato del dispositivo

L'applicazione potrebbe provare a determinare le funzionalità di riproduzione di un dispositivo prima di inviare un file. Se un dispositivo non è in grado di gestire il formato di un file da inviare, l'applicazione potrebbe tentare di eseguire la transcodifica del file in un formato che può essere utilizzato dal dispositivo o inviare una notifica all'utente che il dispositivo non supporta il file richiesto.

Si noti che alcuni dispositivi, ad esempio i dispositivi di classe di archiviazione di massa, possono fungere solo da supporti di archiviazione rimovibili senza funzionalità di riproduzione. In questo caso, sarebbe inappropriato per l'applicazione transcodificare un file prima di inviarlo al dispositivo.

Anche se [**il metodo IWMDMDevice::GetType**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-gettype) consente a un dispositivo di segnalare le proprie funzionalità, alcuni dispositivi restituiscono valori non corretti per questo metodo. Prima di copiare un file in un dispositivo, è possibile chiedere all'utente se la riproduzione è destinata e, in tal caso, tentare di transcodificare il file in uno dei formati segnalati del dispositivo (o in un formato ragionevole, se il dispositivo richiede il supporto per qualsiasi formato). Un altro approccio consiste nel presupporre che tutti i formati elencati in modo specifico come supportati dal dispositivo siano destinati alla riproduzione e che tutti gli altri file debbano essere trasferiti senza modifiche.

Dopo aver scoperto il formato del file da trasferire e i formati supportati da un dispositivo, è possibile decidere quale sia il formato di destinazione migliore per la transcodezione.

In passato, era comune che un'applicazione restituiva zero per una proprietà per indicare il supporto per i valori di tale proprietà. Ad esempio, un valore pari a zero per [**\_ WAVEFORMATEX**](-waveformatex.md).nSamplesPerSec indicherà il supporto per qualsiasi velocità in bit. A questo punto, il modo consigliato per indicare il supporto per qualsiasi valore è specificare WMDM \_ ENUM \_ PROP VALID VALUES ANY in \_ \_ \_ [**WMDM \_ PROP \_ DESC**](wmdm-prop-desc.md). ValidValuesForm. Alcune proprietà, tuttavia, possono restituire legittimamente zero per indicare un supporto specifico. Ad esempio, se [**\_ BITMAPINFOHEADER**](-bitmapinfoheader.md).biSizeImage è impostato su zero, indica una \_ bitmap RGB bi. Le eccezioni per zero valori vengono notate nella documentazione per le strutture pertinenti.

Tuttavia, è importante notare che i dispositivi spesso non segnalano correttamente le funzionalità di formato o in modo standard. Ad esempio, i dispositivi spesso segnalano di supportare qualsiasi formato, quando in realtà possono gestire solo formati specifici o velocità in bit specifiche all'interno di un tipo di formato. È l'utente a decidere se l'applicazione deve accettare tali report o se deve presupporre un tipo di limite superiore alle capacità di riproduzione di un dispositivo (ad esempio, 192 kbps).

Il metodo consigliato per richiedere il supporto del formato di un dispositivo [**è IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability). Se questo metodo non è supportato, l'applicazione deve eseguire il fall back in [**IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport). **GetFormatSupport,** a differenza **di GetFormatSupport2,** non restituisce informazioni video.

Il modo in cui un'applicazione richiede le funzionalità di formato di un dispositivo dipende dall'interfaccia che l'applicazione supporta. Per informazioni dettagliate, vedere gli argomenti seguenti:

-   [Recupero delle funzionalità di formato nei dispositivi che supportano IWMDMDevice3](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
-   [Recupero delle funzionalità di formato nei dispositivi che supportano solo IWMDMDevice](getting-format-capabilities-on-devices-that-support-only-iwmdmdevice.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Scrittura di file nel dispositivo**](writing-files-to-the-device.md)
</dt> </dl>

 

 




