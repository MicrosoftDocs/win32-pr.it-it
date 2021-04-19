---
description: È ora possibile creare automaticamente un mipmap, ovvero una serie di trame, ognuna filtrata per una risoluzione diversa.
ms.assetid: ae5955f9-e52a-41d7-a199-800e37a3e936
title: Generazione automatica di mipmap (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fda5b765d42ffa10f8cc5998daa66ae36c2bc75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304994"
---
# <a name="automatic-generation-of-mipmaps-direct3d-9"></a>Generazione automatica di mipmap (Direct3D 9)

È ora possibile creare automaticamente un mipmap, ovvero una serie di trame, ognuna filtrata per una risoluzione diversa. Mipmap vengono comunemente usati per fornire diversi livelli di dettaglio durante il rendering. La generazione automatica di mipmap al momento della creazione della trama sfrutta i vantaggi dei filtri hardware poiché il mipmap risiede nella memoria video.

Per generare automaticamente un mipmap, impostare una nuova D3DUSAGE di utilizzo [ \_ AUTOGENMIPMAP](d3dusage.md) prima di chiamare [**createTexture**](/windows/desktop/api). La generazione del sottolivello da questo punto in è completamente trasparente per l'applicazione. Solo il livello di trama superiore è accessibile all'applicazione; i sottolivelli di trama non sono accessibili perché verranno creati solo quando sono necessari per il driver. Nei casi in cui la generazione del sottolivello può richiedere molto tempo, usare [**GenerateMipSubLevels**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-generatemipsublevels) per suggerire al driver di generare sottolivelli alla volta appropriati per l'applicazione.

## <a name="mipmap-filtering"></a>Filtro mipmap

[**SetAutoGenFilterType**](/windows/desktop/api) controlla la qualità del filtro durante la generazione automatica. Se si modifica il tipo di filtro, i sottolivelli mipmap e ne determinano la rigenerazione. Usare [**GetAutoGenFilterType**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-getautogenfiltertype) per ottenere il tipo di filtro corrente. Il tipo di filtro predefinito è D3DTEXF \_ Linear. Se il driver non supporta un filtro lineare, il tipo di filtro verrà impostato su punto di D3DTEXF \_ .

Questi metodi non hanno effetto se la trama non viene creata con [D3DUSAGE \_ AUTOGENMIPMAP](d3dusage.md) e non viene restituito alcun errore. Tutti i tipi di filtro supportati dal driver per l'applicazione di filtri di trama regolari sono supportati per la generazione automatico ad eccezione di D3DTEXF \_ None. Per ogni tipo di risorsa, i driver devono supportare tutti i tipi di filtro indicati nei tappi di filtro texture, CubeTexture e Volumetexture corrispondenti.

Per verificare quali tipi di filtro sono supportati, controllare per verificare quali Caps sono supportati dai membri TextureFilterCaps e/o CubeTextureFilterCaps di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="mipmap-support"></a>Supporto di mipmap

[D3DUSAGE \_ AUTOGENMIPMAP](d3dusage.md) è solo un hint e questa operazione viene specificata durante la creazione della trama o quando si chiama [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) non genera un errore in uno dei tipi di interfaccia di driver di dispositivo (DDI).

La chiamata a [**UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) non è valida se l'origine è un mipmap generato automaticamente, ma la destinazione non lo è. L'origine può essere una mipmap generata in modo non automatico e la destinazione può essere un mipmap generato automaticamente. In questo caso, viene aggiornato solo il livello di corrispondenza superiore. Tutti gli altri sottolivelli di origine vengono ignorati. Analogamente, quando l'origine e la destinazione vengono generate automaticamente, viene aggiornato solo il livello di corrispondenza superiore. I sottolivelli dall'origine vengono ignorati e i sottolivelli di destinazione vengono rigenerati.

Per verificare il supporto per la generazione automatica di mipmap, verificare che sia impostato [D3DCAPS2 \_ CANAUTOGENMIPMAP](d3dcaps2.md) . In tal caso, chiamare [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con [D3DUSAGE \_ AUTOGENMIPMAP](d3dusage.md). Se il valore restituito è D3D \_ OK, viene garantita la generazione di mipmap. Se il valore restituito è D3DOK \_ NOAUTOGEN, significa che la chiamata di creazione avrà esito positivo, ma non verrà generato alcun mipmap.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trame Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
