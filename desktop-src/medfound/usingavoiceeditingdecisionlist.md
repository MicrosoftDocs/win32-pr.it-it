---
description: Uso di un elenco di decisioni di modifica per la codifica vocale
ms.assetid: a3d88483-acc9-47cf-8735-f17bd3b4ad57
title: Uso di un elenco di decisioni di modifica per la codifica vocale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970cc40bc5749b9edc1017546020fa3806a9730b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310168"
---
# <a name="using-an-editing-decision-list-for-encoding-voice"></a>Uso di un elenco di decisioni di modifica per la codifica vocale

Un elenco di decisioni di modifica (EDL) indica i dati forniti a un codec che fornisce informazioni sul modo in cui devono essere codificate parti specifiche del contenuto. Il codec Windows Media Audio 9 Voice supporta un semplice EDL in cui è possibile specificare le parti di contenuto che contengono musica. Per impostazione predefinita, il codec rileva i passaggi di musica stessa quando è configurato per codificare contenuto misto. Usare EDL solo se il codec non rileva correttamente i tipi di contenuto.

Per usare un EDL, il codificatore vocale deve essere impostato in modo da codificare il contenuto misto. Configurare la modalità del codec vocale su "mixed" impostando la proprietà [MFPKEY \_ WMAVOICE \_ enc \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) su 2. Impostare EDL usando la proprietà [MFPKEY \_ WMAVOICE \_ enc \_ EDL](mfpkey-wmavoice-enc-edlproperty.md) . Il valore di questa proprietà è una stringa contenente un elenco delimitato da virgole degli intervalli di tempo nel contenuto che deve essere codificato come musica. Il primo elemento dell'elenco è la versione di EDL, che è sempre 1. Il secondo elemento è il numero di sezioni di musica descritte nell'elenco. Il secondo elemento è un numero di coppie di valori uguale al secondo elemento; ogni coppia di valori descrive il punto iniziale e finale di un passaggio di musica nel contenuto, in millisecondi.

Ad esempio, la stringa EDL "1, 4, 1000, 2000, 5000, 6000, 9000, 10000, 13000, 14000" specifica quattro passaggi musicali, ognuno dei quali è un secondo lungo. Se le informazioni nella stringa EDL non sono valide, verranno ignorate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del codec Windows Media Audio 9 Voice](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[Utilizzo di audio](workingwithaudio.md)
</dt> </dl>

 

 



