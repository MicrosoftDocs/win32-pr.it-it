---
title: Individuazione delle funzionalità del formato del dispositivo
description: Individuazione delle funzionalità del formato del dispositivo
ms.assetid: dd139816-dc8c-4e73-9a21-67287bfe6405
keywords:
- Windows Media Gestione dispositivi, funzionalità del dispositivo
- Gestione dispositivi, funzionalità del dispositivo
- Guida per programmatori, funzionalità del dispositivo
- applicazioni desktop, funzionalità del dispositivo
- creazione di applicazioni Windows Media Gestione dispositivi, funzionalità del dispositivo
- scrittura di file nei dispositivi, funzionalità del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0ee05476f6b84bc85bb81cc7cff5815649f5842
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298044"
---
# <a name="discovering-device-format-capabilities"></a>Individuazione delle funzionalità del formato del dispositivo

L'applicazione potrebbe provare a determinare le funzionalità di riproduzione di un dispositivo prima di inviare un file. Se un dispositivo non è in grado di gestire il formato di un file che si vuole inviare, l'applicazione potrebbe provare a transcodificare il file in un formato che il dispositivo può usare oppure informare l'utente che il dispositivo non può supportare il file richiesto.

Si noti che alcuni dispositivi, ad esempio i dispositivi della classe di archiviazione di massa, possono fungere solo da supporti di archiviazione rimovibili senza funzionalità di riproduzione. In questo caso, non sarebbe appropriato per l'applicazione eseguire la transcodifica di un file prima di inviarlo al dispositivo.

Sebbene il metodo [**IWMDMDevice:: GetType**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-gettype) consenta a un dispositivo di segnalare le proprie funzionalità, alcuni dispositivi restituiscono valori non corretti per questo metodo. Prima di copiare un file in un dispositivo, potrebbe essere necessario chiedere all'utente se la riproduzione è intenzionale e, in tal caso, provare a transcodificare il file in uno dei formati segnalati del dispositivo (o in un formato ragionevole se il dispositivo richiede il supporto per qualsiasi formato). Un altro approccio consiste nel presupporre che tutti i formati elencati in modo specifico come supportati dal dispositivo siano destinati alla riproduzione e che tutti gli altri file vengano trasferiti senza modifiche.

Dopo aver individuato il formato del file da trasferire e i formati supportati da un dispositivo, è possibile decidere quale sia il formato di destinazione migliore per la transcodifica.

In passato era comune per un'applicazione restituire zero per una proprietà, in modo da indicare il supporto per tutti i valori della proprietà. Ad esempio, un valore pari a zero per [**\_ WAVEFORMATEX**](-waveformatex.md). nSamplesPerSec indicherà il supporto per qualsiasi velocità in bit. A questo punto, il metodo consigliato per indicare il supporto per qualsiasi valore consiste nel specificare WMDM \_ enum \_ prop \_ valid \_ Values \_ any in [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md). ValidValuesForm. Alcune proprietà, tuttavia, possono restituire in modo legittimo zero per indicare un supporto specifico. Ad esempio, se [**\_ BITMAPINFOHEADER**](-bitmapinfoheader.md). biSizeImage è impostato su zero, indica una \_ bitmap RGB bi. Le eccezioni per i valori zero sono indicate nella documentazione per le strutture pertinenti.

Tuttavia, è importante notare che i dispositivi spesso non segnalano correttamente le proprie funzionalità di formato o in modo standard. Ad esempio, i dispositivi spesso segnalano che supportano qualsiasi formato, quando in realtà possono gestire solo formati specifici o frequenze di bit specifiche all'interno di un tipo di formato. È necessario decidere se l'applicazione deve accettare tali report o se deve presupporre un certo tipo di limite superiore alle capacità di riproduzione di un dispositivo, ad esempio 192 kbps.

Il metodo consigliato per la richiesta del supporto del formato del dispositivo è [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability). Se questo metodo non è supportato, l'applicazione deve eseguire il fallback in [**IWMDMDevice:: GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport). **GetFormatSupport**, a differenza di **GetFormatSupport2**, non restituisce informazioni sul video.

Il modo in cui un'applicazione richiede le funzionalità di formato del dispositivo dipende dall'interfaccia supportata dall'applicazione. Per informazioni dettagliate, vedere gli argomenti seguenti:

-   [Ottenere le funzionalità di formato nei dispositivi che supportano IWMDMDevice3](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
-   [Ottenere le funzionalità di formato nei dispositivi che supportano solo IWMDMDevice](getting-format-capabilities-on-devices-that-support-only-iwmdmdevice.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Scrittura di file nel dispositivo**](writing-files-to-the-device.md)
</dt> </dl>

 

 




