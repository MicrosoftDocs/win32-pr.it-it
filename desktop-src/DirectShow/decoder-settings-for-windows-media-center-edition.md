---
description: Decodificatore Impostazioni per Windows Media Center Edition
ms.assetid: 019b063f-f215-44d8-a916-3125bee6af93
title: Decodificatore Impostazioni per Windows Media Center Edition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc373f2ea58bc169748ff42841650cf979822014e579a78459e47da5c694814
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953160"
---
# <a name="decoder-settings-for-windows-media-center-edition"></a>Decodificatore Impostazioni per Windows Media Center Edition

Windows XP Media Center Edition 2005 e versioni successive usa [**l'interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) per configurare il filtro del decodificatore audio per la riproduzione tv e DVD. Sono supportate le proprietà seguenti.



| GUID proprietà                   | Descrizione                                      |
|---------------------------------|--------------------------------------------------|
| FORMATO DI \_ OUTPUT AUDIO CODECAPI \_ \_ | Configura il formato di output audio. Vedere la sezione Osservazioni. |



 

## <a name="remarks"></a>Commenti

Il valore della proprietà CODECAPI AUDIO OUTPUT FORMAT è una rappresentazione di stringa di \_ \_ un \_ GUID, archiviata come **valore BSTR.** Vengono definiti i GUID seguenti.



| GUID                                                        | Descrizione                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MATRICE STEREO \_ \_ PCM IN FORMATO DI OUTPUT AUDIO \_ \_ \_ \_ CODECAPIENCODED | Il filtro audio software deve eseguire la decodifica software e l'output di un flusso audio stereo, con la matrice audio multicanale codificata nei due canali.                                                   |
| FORMATO DI \_ OUTPUT AUDIO CODECAPI \_ \_ \_ PCM \_ STEREO                | Il filtro audio software deve eseguire la decodifica software e l'output di un flusso audio stereo.                                                                                                                   |
| FORMATO DI \_ OUTPUT AUDIO CODECAPI \_ \_ \_ SPDIF \_ PCM                 | Il filtro audio software deve eseguire la decodifica audio software, anche se l'output fisico del PC può essere un'interfaccia digitale, ad esempio S/PDIF.                                                      |
| FORMATO DI \_ OUTPUT AUDIO CODECAPI \_ \_ \_ SPDIF \_ BITSTREAM           | Il filtro audio software non deve eseguire la decodifica audio software, ma deve passare il flusso di bit audio digitale non elaborato per l'elaborazione esterna da parte di un dispositivo connesso con un collegamento audio digitale, ad esempio S/PDIF. |
| HEAD \_ \_ \_ \_ PCM IN FORMATO DI OUTPUT AUDIO CODECAPI \_            | Il filtro audio software deve eseguire la decodifica audio software e applicare l'elaborazione proprietaria per ottimizzare le cuffi. Il supporto per questa impostazione è facoltativo.                                     |



 

> [!Note]  
> **L'interfaccia ICodecAPI** archivia le proprietà del codec come coppie chiave/valore, dove la chiave è un GUID e il valore è un **tipo VARIANT.**

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di codificatori e decodificatori](encoder-and-decoder-development.md)
</dt> </dl>

 

 



