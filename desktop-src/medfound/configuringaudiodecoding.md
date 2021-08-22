---
description: Configurazione della decodifica audio
ms.assetid: 362bd3bc-1474-4132-a8a8-e5dc0bba80e7
title: Configurazione della decodifica audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee274fd714065a1c89c9d634dd80de4d59c9eb567d67ed8045d2b89bece87d74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664647"
---
# <a name="configuring-audio-decoding-microsoft-media-foundation"></a>Configurazione della decodifica audio (Microsoft Media Foundation)

La decodifica Windows contenuto audio multimediale è molto più semplice rispetto alla codifica. Dopo aver creato un oggetto decodificatore audio, impostare il tipo di input usando il metodo **IMediaObject::SetInputType** o **IMFTransform::SetInputType.** Il tipo di supporto usato per l'input del decodificatore deve corrispondere al tipo di output utilizzato durante la codifica del contenuto. Sono inclusi i dati in formato esteso aggiunti alla **struttura WAVEFORMATEX.** È necessario assicurarsi che questi dati siano corretti, perché il decodificatore non è in grado di elaborare i campioni senza di esso.

Dopo aver impostato il tipo di input, è possibile configurare le funzionalità del decodificatore da usare. Le funzionalità del decodificatore, come quelle usate per la codifica, vengono impostate usando i metodi **di IPropertyBag** **o IPropertyStore.**

Dopo aver impostato il tipo di input e configurato tutte le funzionalità del decodificatore, è possibile enumerare i tipi di output supportati dal decodificatore effettuando chiamate a **IMediaObject::GetOutputType** o **IMFTransform::GetOutputType**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'audio](workingwithaudio.md)
</dt> </dl>

 

 



