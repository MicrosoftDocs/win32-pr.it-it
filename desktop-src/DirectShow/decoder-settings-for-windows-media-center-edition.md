---
description: Impostazioni del decodificatore per Windows Media Center Edition
ms.assetid: 019b063f-f215-44d8-a916-3125bee6af93
title: Impostazioni del decodificatore per Windows Media Center Edition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f66b5107fa0316f6ce2547e1f5f066165ed598
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320695"
---
# <a name="decoder-settings-for-windows-media-center-edition"></a>Impostazioni del decodificatore per Windows Media Center Edition

Windows XP Media Center Edition 2005 e versioni successive utilizza l'interfaccia [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) per configurare il filtro del decodificatore audio per la riproduzione TV e DVD. Sono supportate le proprietà seguenti.



| GUID proprietà                   | Descrizione                                      |
|---------------------------------|--------------------------------------------------|
| formato di \_ output audio CODEcapis \_ \_ | Configura il formato di output audio. Vedere la sezione Osservazioni. |



 

## <a name="remarks"></a>Commenti

Il valore della \_ proprietà formato output audio CODEcapites \_ \_ è una rappresentazione di stringa di un GUID, archiviato come valore **BSTR** . Sono definiti i seguenti GUID.



| GUID                                                        | Descrizione                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| formato di output audio di codecapis \_ \_ \_ \_ PCM \_ stereo \_ MATRIXENCODED | Il filtro audio software deve eseguire la decodifica del software e restituire un flusso audio stereo con la matrice audio multicanale codificata nei due canali.                                                   |
| formato di output audio di codecapis \_ \_ \_ \_ PCM \_ stereo                | Il filtro audio software deve eseguire la decodifica software e restituire un flusso audio stereo.                                                                                                                   |
| formato output audio codecapis ( \_ \_ \_ PCM) \_ SPDIF \_                 | Il filtro audio software deve eseguire la decodifica audio software, anche se l'output fisico del PC può essere un'interfaccia digitale, ad esempio S/PDIF.                                                      |
| formato di output audio di codecapis \_ \_ \_ \_ SPDIF \_ Bitstream           | Il filtro audio software non deve eseguire la decodifica audio software, ma deve passare il bitstream audio digitale non elaborato per l'elaborazione esterna da parte di un dispositivo connesso a un collegamento audio digitale, ad esempio S/PDIF. |
| \_ \_ \_ \_ cuffie PCM formato output audio codecapis \_            | Il filtro audio software deve eseguire la decodifica audio software e deve applicare l'elaborazione proprietaria per ottimizzare le cuffie. Il supporto per questa impostazione è facoltativo.                                     |



 

> [!Note]  
> L'interfaccia **ICodecAPI** archivia le proprietà dei codec come coppie chiave/valore, dove la chiave è un GUID e il valore è un tipo **Variant** .

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di codificatori e decodificatori](encoder-and-decoder-development.md)
</dt> </dl>

 

 



