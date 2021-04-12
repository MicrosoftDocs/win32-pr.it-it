---
description: Microsoft DirectX Graphics Infrastructure (DXGI) gestisce le attività di basso livello che possono essere indipendenti dal runtime di grafica Direct3D. DXGI fornisce un Framework comune per diverse versioni di Direct3D.
ms.assetid: bcbeb4bc-3bd1-40ed-b176-a8091cc6ee9f
title: Guida per programmatori per DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7834b2fc68019dccfb8ab8b2e62698465ff1ea2d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225329"
---
# <a name="programming-guide-for-dxgi"></a>Guida per programmatori per DXGI

Microsoft DirectX Graphics Infrastructure (DXGI) gestisce le attività di basso livello che possono essere indipendenti dal runtime di grafica Direct3D. DXGI fornisce un Framework comune per diverse versioni di Direct3D.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                              | Descrizione                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Panoramica di DXGI](d3d10-graphics-programming-guide-dxgi.md)<br/>                                                              | In questo argomento sono contenute le sezioni seguenti.<br/>                                                                                                                   |
| [Miglioramenti di DXGI 1,2](dxgi-1-2-improvements.md)<br/>                                                                      | In DXGI 1,2 sono state aggiunte le funzionalità seguenti.<br/>                                                                                                       |
| [Miglioramenti di DXGI 1,3](dxgi-1-3-improvements.md)<br/>                                                                      | Le funzionalità seguenti sono state aggiunte in DXGI 1,3, incluso a partire da Windows 8.1.<br/>                                                            |
| [Miglioramenti di DXGI 1,4](dxgi-1-4-improvements.md)<br/>                                                                      | Le funzionalità seguenti sono state aggiunte o modificate in DXGI 1,4, in gran parte per supportare Direct3D 12. <br/>                                                           |
| [Miglioramenti di DXGI 1,5](dxgi-1-5-improvements.md)<br/>                                                                      | Le funzionalità seguenti sono state aggiunte a DXGI 1,5, per supportare la specifica e la duplicazione più flessibili dei formati di output.<br/>                                |
| [Miglioramenti di DXGI 1,6](dxgi-1-6-improvements.md)<br/>                                                                      | Le funzionalità seguenti sono state aggiunte a DXGI 1,6 per poter rilevare le visualizzazioni HDR.<br/>                                                                       |
| [Uso di DirectX con schermi HDR e colori avanzati](../direct3darticles/high-dynamic-range.md)     | In questo argomento viene fornita una panoramica tecnica sul rendering di contenuti High Dynamic Range Direct3D 11 e Direct3D 12 in una visualizzazione HDR10 con il supporto dei colori avanzati di Windows 10.<br/> |
| [Visualizzazione frequenza di aggiornamento variabili](variable-refresh-rate-displays.md)<br/>                                                    | Le visualizzazioni della frequenza di aggiornamento variabili richiedono l'abilitazione dello *strappo* , noto anche come supporto "VSync".<br/>                                                    |
| [Uso della correzione gamma](using-gamma-correction.md)<br/>                                                                    | La correzione gamma o la gamma Short è il nome di un'operazione non lineare utilizzata dai sistemi per codificare e decodificare i valori dei pixel nelle immagini.<br/>                        |
| [Supporto del formato per la funzionalità Direct3D 10Level9 9,1 hardware](format-support-for-direct3d-feature-level-9-1-hardware.md)<br/> | Questa sezione specifica i formati (valori di [**\_ formato DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) supportati nell'hardware della funzionalità Direct3D 10Level9 9,1.<br/>        |
| [Supporto del formato per la funzionalità Direct3D 10Level9 9,3 hardware](format-support-for-direct3d-feature-level-9-3-hardware.md)<br/> | Questa sezione specifica i formati (valori di [**\_ formato DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) supportati nell'hardware della funzionalità Direct3D 10Level9 9,3.<br/>        |
| [Supporto del formato per l'hardware a livello di funzionalità Direct3D 10,0](format-support-for-direct3d-feature-level-10-0-hardware.md)<br/>  | Questa sezione specifica i formati (valori di [**\_ formato DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) supportati nell'hardware Direct3D 10,0.<br/>                        |
| [Supporto del formato per l'hardware a livello di funzionalità Direct3D 10,1](format-support-for-direct3d-feature-level-10-1-hardware.md)<br/>  | Questa sezione specifica i formati (valori di [**\_ formato DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) supportati nell'hardware Direct3D 10,1.<br/>                        |
| [Supporto del formato per l'hardware a livello di funzionalità Direct3D 11,0](format-support-for-direct3d-11-0-feature-level-hardware.md)<br/>  | Questa sezione specifica i formati (valori di [**\_ formato DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) supportati nell'hardware del livello di funzionalità Direct3D 11,0.<br/>          |
| [Supporto del formato per l'hardware a livello di funzionalità Direct3D 11,1](format-support-for-direct3d-11-1-feature-level-hardware.md)<br/>  | Questa sezione specifica i formati (valori di [**\_ formato DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) supportati nell'hardware del livello di funzionalità Direct3D 11,1.<br/>          |
| [Supporto del formato per l'hardware a livello di funzionalità Direct3D 12,0](hardware-support-for-direct3d-12-0-formats.md)<br/>               | Questa sezione specifica i formati (valori di [**\_ formato DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) supportati nell'hardware del livello di funzionalità Direct3D 12,0.<br/>          |
| [Supporto del formato per l'hardware a livello di funzionalità Direct3D 12,1](hardware-support-for-direct3d-12-1-formats.md)<br/>               | Questa sezione specifica i formati (valori di [**\_ formato DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) supportati nell'hardware Direct3D 12,1.<br/>                        |
| [Verifica del supporto delle funzionalità hardware](checking-hardware-feature-support.md)<br/>                                              | Questa sezione illustra come verificare il supporto del formato per l'hardware a livello di funzionalità Direct3D usando le chiamate API.<br/>                                                       |
| [Per ottenere prestazioni ottimali, usare DXGI flip model](for-best-performance--use-dxgi-flip-model.md)<br/>                              | Questo argomento fornisce indicazioni per gli sviluppatori su come ottimizzare le prestazioni e l'efficienza nello stack di presentazione nelle versioni moderne di Windows.<br/>                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DXGI](dx-graphics-dxgi.md)
</dt> <dt>

[Riferimento a DXGI](d3d10-graphics-reference-dxgi.md)
</dt> <dt>

[Infrastruttura grafica DirectX (DXGI): procedure consigliate](../direct3darticles/dxgi-best-practices.md)
</dt> </dl>

 

 
