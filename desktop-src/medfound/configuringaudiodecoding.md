---
description: Configurazione della decodifica audio
ms.assetid: 362bd3bc-1474-4132-a8a8-e5dc0bba80e7
title: Configurazione della decodifica audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da4d6a9d41b5c504ff60f25db20265072218caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749330"
---
# <a name="configuring-audio-decoding-microsoft-media-foundation"></a>Configurazione della decodifica audio (Microsoft Media Foundation)

La decodifica Windows Media Audio contenuto è molto più semplice rispetto alla codifica. Dopo aver creato un oggetto Decoder audio, impostare il tipo di input usando il metodo **IMediaObject:: SetInputType** o **IMFTransform:: SetInputType** . Il tipo di supporto utilizzato per l'input del decodificatore deve corrispondere al tipo di output utilizzato durante la codifica del contenuto. Sono inclusi i dati in formato esteso aggiunti alla struttura **WAVEFORMATEX** . È necessario assicurarsi che questi dati siano corretti, perché il decodificatore non è in grado di elaborare esempi senza di esso.

Dopo aver impostato il tipo di input, è possibile configurare tutte le funzionalità di decodificatore che si desidera utilizzare. Le funzionalità di decodificatore, come quelle usate per la codifica, vengono impostate usando i metodi di **IPropertyBag** o **IPropertyStore**.

Dopo aver impostato il tipo di input e aver configurato tutte le funzionalità del decodificatore, è possibile enumerare i tipi di output supportati dal decodificatore effettuando chiamate a **IMediaObject:: GetOutputType** o **IMFTransform:: GetOutputType**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di audio](workingwithaudio.md)
</dt> </dl>

 

 



