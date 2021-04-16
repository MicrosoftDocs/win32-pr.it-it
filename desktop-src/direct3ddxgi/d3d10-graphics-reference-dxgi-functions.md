---
description: Questa sezione contiene informazioni sulle funzioni fornite da DXGI.
ms.assetid: 209d2e65-b118-47a7-aece-fb140fdede3f
title: Funzioni DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06cb98c47ec3e2cb841aa5c27017ee6bb614f9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520874"
---
# <a name="dxgi-functions"></a>Funzioni DXGI

Questa sezione contiene informazioni sulle funzioni fornite da DXGI.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDXGIFactory**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory)<br/>                               | Crea una factory DXGI 1,0 che è possibile usare per generare altri oggetti DXGI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**CreateDXGIFactory1**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1)<br/>                             | Crea una factory DXGI 1,1 che è possibile usare per generare altri oggetti DXGI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2)<br/>                             | Crea una factory DXGI 1,3 che è possibile usare per generare altri oggetti DXGI.<br/> In Windows 8, qualsiasi Factory di DXGI creata durante la DXGIDebug.dll era presente nel sistema, la caricherà e la utilizzerebbe. A partire da Windows 8.1, le app richiedono in modo esplicito che DXGIDebug.dll venga caricato. Usare [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) e specificare il \_ \_ \_ flag di debug di DXGI create Factory per richiedere DXGIDebug.dll; la dll verrà caricata se presente nel sistema.<br/> |
| [**DXGIDeclareAdapterRemovalSupport**](/windows/desktop/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport)<br/> | Consente a un processo di indicare che è resiliente per i dispositivi grafici da rimuovere.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [**DXGIGetDebugInterface**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)<br/>                       | Recupera un'interfaccia di debug.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**DXGIGetDebugInterface1**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-dxgigetdebuginterface1)<br/>                     | Recupera un'interfaccia utilizzata dalle app di Windows Store per il debug di Microsoft DirectX Graphics Infrastructure (DXGI).<br/>                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento a DXGI](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

 




