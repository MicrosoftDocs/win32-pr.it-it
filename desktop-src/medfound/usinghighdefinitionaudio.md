---
description: Uso di High-Definition audio
ms.assetid: 5e21943f-363c-4831-bc09-aadf6f4a0ad5
title: Uso di High-Definition audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05e7bd9311574c3d25f9069ea60c9d269d24390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755239"
---
# <a name="using-high-definition-audio-microsoft-media-foundation"></a>Uso di High-Definition audio (Microsoft Media Foundation)

L'audio ad alta definizione, nel contesto dei codec di Windows Media Audio, è qualsiasi tipo di audio con più di due canali o più di 16 bit per campione. L'audio ad alta definizione è supportato dalle categorie Professional e lossless del [codificatore Windows Media Audio](windowsmediaaudioencoder.md).

I tipi audio ad alta definizione non compressi vengono definiti usando la struttura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) . **WAVEFORMATEXTENSIBLE** è un'estensione strutturata della struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) . Quando si usa DMOs, il membro **formatType** della struttura del [**\_ \_ tipo di supporto DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) che descrive un tipo audio ad alta definizione deve essere impostato su WMCFORMAT \_ WAVEFORMATEX, così come per l'audio normale. non esiste alcun identificatore di formato speciale per **WAVEFORMATEXTENSIBLE**. Se un formato USA **WAVEFORMATEXTENSIBLE** , è necessario impostare il membro **cbSize** della struttura **WAVEFORMATEX** su 22.

Quando si usa Media Foundation, è possibile costruire il tipo di supporto corretto da una struttura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) usando la funzione [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex).

I tipi di output multicanale supportati dal codec Windows Media Audio 10 Professional non usano [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)), ma segnalano il numero corretto di canali e BITS per campione nella struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) . Come per tutti i tipi audio che descrivono il contenuto compresso di Windows Media Audio, sono presenti informazioni aggiuntive aggiunte alla struttura **WAVEFORMATEX** usata dal decodificatore per la decompressione.

## <a name="decoding-high-definition-audio"></a>Decodifica audio High-Definition

Per decodificare l'audio ad alta definizione, è necessario impostare la proprietà [MFPKEY \_ WMADEC \_ HIRESOUTPUT](mfpkey-wmadec-hiresoutputproperty.md) su Variant \_ true. Se questa proprietà non è impostata, il decodificatore fornirà contenuto stereo con un massimo di 16 bit per campione, indipendentemente dal formato compresso.

> [!Note]  
> L'audio ad alta definizione è supportato solo per Windows XP, Windows Vista e versioni successive. Nelle versioni precedenti di Windows, il contenuto Windows Media Audio codificato con definizione alta viene visualizzato come audio a due canali con un massimo di 16 bit per campione.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di audio](workingwithaudio.md)
</dt> </dl>

 

 
