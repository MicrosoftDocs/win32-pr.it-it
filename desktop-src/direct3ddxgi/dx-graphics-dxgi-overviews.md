---
description: Microsoft DirectX Graphic Infrastructure (DXGI) gestisce attività di basso livello che possono essere indipendenti dal runtime di grafica Direct3D. DXGI offre un framework comune per diverse versioni di Direct3D.
ms.assetid: bcbeb4bc-3bd1-40ed-b176-a8091cc6ee9f
title: Guida per programmatori per DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0ac41155557c14ca41f8e0ea9f1836247bd3b78da213c1fbbed521499eae7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518384"
---
# <a name="programming-guide-for-dxgi"></a>Guida per programmatori per DXGI

Microsoft DirectX Graphic Infrastructure (DXGI) gestisce attività di basso livello che possono essere indipendenti dal runtime di grafica Direct3D. DXGI offre un framework comune per diverse versioni di Direct3D.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                              | Descrizione                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Panoramica di DXGI](d3d10-graphics-programming-guide-dxgi.md)<br/>                                                              | In questo argomento sono contenute le sezioni seguenti.<br/>                                                                                                                   |
| [Miglioramenti di DXGI 1.2](dxgi-1-2-improvements.md)<br/>                                                                      | La funzionalità seguente è stata aggiunta in DXGI 1.2.<br/>                                                                                                       |
| [Miglioramenti di DXGI 1.3](dxgi-1-3-improvements.md)<br/>                                                                      | La funzionalità seguente è stata aggiunta in DXGI 1.3, inclusa a partire da Windows 8.1.<br/>                                                            |
| [Miglioramenti di DXGI 1.4](dxgi-1-4-improvements.md)<br/>                                                                      | La funzionalità seguente è stata aggiunta o modificata in DXGI 1.4, in gran parte per supportare Direct3D 12. <br/>                                                           |
| [Miglioramenti di DXGI 1.5](dxgi-1-5-improvements.md)<br/>                                                                      | La funzionalità seguente è stata aggiunta a DXGI 1.5 per supportare la specifica e la duplicazione dei formati di output più flessibili.<br/>                                |
| [Miglioramenti di DXGI 1.6](dxgi-1-6-improvements.md)<br/>                                                                      | La funzionalità seguente è stata aggiunta a DXGI 1.6 per rilevare gli schermi HDR.<br/>                                                                       |
| [Uso di DirectX con schermi HDR e colori avanzati](../direct3darticles/high-dynamic-range.md)     | Questo argomento offre una panoramica tecnica del rendering di contenuto Direct3D 11 e Direct3D 12 a un display HDR10 usando Windows 10 di colore avanzato.<br/> |
| [Visualizzazione della frequenza di aggiornamento variabile](variable-refresh-rate-displays.md)<br/>                                                    | Le frequenze di aggiornamento variabili richiedono che sia abilitato lo *tearing.* Questo supporto è noto anche come "vsync-off".<br/>                                                    |
| [Uso della correzione gamma](using-gamma-correction.md)<br/>                                                                    | Correzione gamma, o gamma per brevi, è il nome di un'operazione non lineare che i sistemi usano per codificare e decodificare i valori dei pixel nelle immagini.<br/>                        |
| [Supporto del formato per l'hardware Direct3D Feature 10Level9 9.1](format-support-for-direct3d-feature-level-9-1-hardware.md)<br/> | Questa sezione specifica i formati [**(valori DXGI \_ FORMAT)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) supportati nell'hardware Direct3D Feature 10Level9 9.1.<br/>        |
| [Supporto del formato per l'hardware Direct3D Feature 10Level9 9.3](format-support-for-direct3d-feature-level-9-3-hardware.md)<br/> | Questa sezione specifica i formati [**(valori DXGI \_ FORMAT)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) supportati nell'hardware Direct3D Feature 10Level9 9.3.<br/>        |
| [Supporto del formato per l'hardware Direct3D Feature Level 10.0](format-support-for-direct3d-feature-level-10-0-hardware.md)<br/>  | Questa sezione specifica i formati [**(valori DXGI \_ FORMAT)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) supportati nell'hardware Direct3D 10.0.<br/>                        |
| [Supporto del formato per l'hardware Direct3D Feature Level 10.1](format-support-for-direct3d-feature-level-10-1-hardware.md)<br/>  | Questa sezione specifica i formati [**(valori DXGI \_ FORMAT)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) supportati nell'hardware Direct3D 10.1.<br/>                        |
| [Supporto del formato per l'hardware Direct3D Feature Level 11.0](format-support-for-direct3d-11-0-feature-level-hardware.md)<br/>  | Questa sezione specifica i formati [**(valori DXGI \_ FORMAT)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) supportati nell'hardware Direct3D Feature Level 11.0.<br/>          |
| [Supporto del formato per l'hardware Direct3D Feature Level 11.1](format-support-for-direct3d-11-1-feature-level-hardware.md)<br/>  | Questa sezione specifica i formati [**(valori DXGI \_ FORMAT)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) supportati nell'hardware Direct3D Feature Level 11.1.<br/>          |
| [Supporto del formato per l'hardware Direct3D Feature Level 12.0](hardware-support-for-direct3d-12-0-formats.md)<br/>               | Questa sezione specifica i formati [**(valori DXGI \_ FORMAT)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) supportati nell'hardware Direct3D Feature Level 12.0.<br/>          |
| [Supporto del formato per l'hardware Direct3D Feature Level 12.1](hardware-support-for-direct3d-12-1-formats.md)<br/>               | Questa sezione specifica i formati [**(valori DXGI \_ FORMAT)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) supportati nell'hardware Direct3D 12.1.<br/>                        |
| [Controllo del supporto delle funzionalità hardware](checking-hardware-feature-support.md)<br/>                                              | Questa sezione illustra come controllare il supporto del formato per l'hardware a livello di funzionalità Direct3D tramite chiamate API.<br/>                                                       |
| [Per prestazioni ottimali, usare il modello flip DXGI](for-best-performance--use-dxgi-flip-model.md)<br/>                              | Questo argomento fornisce indicazioni per gli sviluppatori su come ottimizzare le prestazioni e l'efficienza nello stack di presentazione nelle versioni moderne di Windows.<br/>                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DXGI](dx-graphics-dxgi.md)
</dt> <dt>

[Informazioni di riferimento su DXGI](d3d10-graphics-reference-dxgi.md)
</dt> <dt>

[DirectX Graphic Infrastructure (DXGI): Procedure consigliate](../direct3darticles/dxgi-best-practices.md)
</dt> </dl>

 

 
