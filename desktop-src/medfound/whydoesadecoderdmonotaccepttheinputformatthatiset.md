---
description: Perché un decodificatore non accetta il formato di input impostato?
ms.assetid: 19aa5677-bc3f-41d7-ad64-7c75021d907b
title: Perché un decodificatore non accetta il formato di input impostato?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32ae4506fb6ed940bf0b4fffcf82ab78562872d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310156"
---
# <a name="why-does-a-decoder-not-accept-the-input-format-that-i-set"></a>Perché un decodificatore non accetta il formato di input impostato?

Esistono molti motivi per cui un decodificatore potrebbe rifiutare un formato. I dati in formato esteso mancanti o non corretti sono i più comuni. I dati di formato esteso sono informazioni specifiche del codec aggiunte alla struttura che descrive il tipo di supporto.

Quando si enumera un tipo di output usando un oggetto Encoder, il membro **pbFormat** della struttura del [**\_ \_ tipo di supporto DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) punterà a una struttura **WAVEFORMATEX** . A questa struttura sono stati aggiunti dati in formato esteso e le dimensioni dei dati vengono archiviate nel membro **WAVEFORMATEX. cbSize** . Indipendentemente dal contenitore utilizzato per archiviare i dati compressi, è necessario salvare in modo permanente la struttura **WAVEFORMATEX** e utilizzarla nel tipo di input per il decodificatore. Senza i dati di formato esteso, il decodificatore non può decomprimere il contenuto.

Per i formati video, è necessario recuperare manualmente i dati in formato esteso e aggiungerli alla struttura **VIDEOINFOHEADER** . Per altre informazioni, vedere [uso di dati privati di codec video](usingvideocodecprivatedata.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Domande frequenti](frequentlyaskedquestions.md)
</dt> </dl>

 

 
