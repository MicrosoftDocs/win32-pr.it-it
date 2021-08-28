---
description: Questa sezione specifica i formati [**(DXGI_FORMAT_)** *](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) supportati nell'hardware Direct3D Feature Level 12.1.
ms.assetid: 0DC50FF3-3193-4F3B-9976-EE504C6FCC87
title: Supporto del formato per l'hardware a livello di funzionalità 12.1 di Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 065192ffadf8667f82c0e1b0fc6fac165f103a7ed28982cba1fbc0e14ae47cce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068761"
---
# <a name="format-support-for-direct3d-feature-level-121-hardware"></a>Supporto del formato per l'hardware a livello di funzionalità 12.1 di Direct3D

Questa sezione specifica i formati [**(DXGI_FORMAT_)** *](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) supportati nell'hardware Direct3D Feature Level 12.1.

La tabella riepiloga il supporto delle funzionalità usando la chiave seguente.

| Simbolo                            | Descrizione                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| **-**                             | Non consentito o non disponibile.                                                  |
| ![necessario](images/letter-r.jpg)  | È necessario il supporto hardware.                                                 |
| ![facoltative](images/letter-o.jpg)  | Supporto hardware facoltativo. Il formato può essere accelerato o meno dall'hardware. |
| ![Dipendente](images/letter-d.jpg) | Obbligatorio se è supportata la funzionalità facoltativa correlata.                            |

Questo argomento contiene una sezione per ogni formato. Una destinazione *di* formato (le tabelle contengono una riga per ogni destinazione) può essere un tipo di risorsa, una funzione intrinseca HLSL o una particolare funzionalità dipendente da un formato specifico.

Per verificare a livello di codice il supporto del formato in D3D11 e D3D12, vedere [Controllo del supporto delle funzionalità hardware](checking-hardware-feature-support.md).

> [!NOTE] 
> I numeri dei formati sono principalmente, ma non tutti, in ordine numerico crescente, alcuni non sono in ordine numerico ed elencati insieme ad &mdash; altri formati rilevanti. Si noti *anche* che senza tipo  in un nome di formato può significare [](#format-notes) parzialmente tipi di dati e non rigorosamente senza tipi (vedere la sezione Formattare le note alla fine dell'argomento).

## <a name="dxgi_format_unknownsuplsup-0"></a>DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 0 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | ![necessario](images/letter-r.jpg) |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a>DXGI_FORMAT_R32G32B32A32_TYPELESS<sup>PCS</sup> (1)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a>DXGI_FORMAT_R32G32B32A32_FLOAT<sup>FCS</sup> (2)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| Archivio tipidato UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![necessario](images/letter-r.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a>DXGI_FORMAT_R32G32B32A32_UINT<sup>FCS</sup> (3)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | ![necessario](images/letter-r.jpg) |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![necessario](images/letter-r.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a>DXGI_FORMAT_R32G32B32A32_SINT<sup>FCS</sup> (4)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| Archivio tipidato UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![necessario](images/letter-r.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a>DXGI_FORMAT_R32G32B32_TYPELESS<sup>PCS</sup> (5)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 96 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a>DXGI_FORMAT_R32G32B32_FLOAT<sup>FCS</sup> (6)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 96 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![facoltative](images/letter-o.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![facoltative](images/letter-o.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![facoltative](images/letter-o.jpg) |
| RenderTarget | ![facoltative](images/letter-o.jpg) |
| Blendable RenderTarget | ![Dipendente](images/letter-d.jpg) |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Dipendente](images/letter-d.jpg) |
| 8x Multisample RenderTarget | ![Dipendente](images/letter-d.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a>DXGI_FORMAT_R32G32B32_UINT<sup>FCS</sup> (7)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 96 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![facoltative](images/letter-o.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | ![necessario](images/letter-r.jpg) |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Dipendente](images/letter-d.jpg) |
| 8x Multisample RenderTarget | ![Dipendente](images/letter-d.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a>DXGI_FORMAT_R32G32B32_SINT<sup>FCS</sup> (8)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 96 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![facoltative](images/letter-o.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Dipendente](images/letter-d.jpg) |
| 8x Multisample RenderTarget | ![Dipendente](images/letter-d.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a>DXGI_FORMAT_R16G16B16A16_TYPELESS<sup>PCS</sup> (9)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a>DXGI_FORMAT_R16G16B16A16_FLOAT<sup>FCS</sup> (10)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| Archivio tipidato UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![necessario](images/letter-r.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | ![necessario](images/letter-r.jpg) |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![necessario](images/letter-r.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a>DXGI_FORMAT_R16G16B16A16_UNORM<sup>FCS</sup> (11)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a>DXGI_FORMAT_R16G16B16A16_UINT<sup>FCS</sup> (12)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | ![necessario](images/letter-r.jpg) |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![necessario](images/letter-r.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a>DXGI_FORMAT_R16G16B16A16_SNORM<sup>FCS</sup> (13)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a>DXGI_FORMAT_R16G16B16A16_SINT<sup>FCS</sup> (14)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![necessario](images/letter-r.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a>DXGI_FORMAT_R32G32_TYPELESS<sup>PCS</sup> (15)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a>DXGI_FORMAT_R32G32_FLOAT<sup>FCS</sup> (16)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a>DXGI_FORMAT_R32G32_UINT<sup>FCS</sup> (17)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | ![necessario](images/letter-r.jpg) |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a>DXGI_FORMAT_R32G32_SINT<sup>FCS</sup> (18)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32g8x24_typelesssupvsup-19"></a>DXGI_FORMAT_R32G8X24_TYPELESS<sup>V</sup> (19)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupvsup-20"></a>DXGI_FORMAT_D32_FLOAT_S8X24_UINT<sup>V</sup> (20)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | ![necessario](images/letter-r.jpg) |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupvsup-21"></a>DXGI_FORMAT_R32_FLOAT_X8X24_TYPELESS<sup>V</sup> (21)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | ![necessario](images/letter-r.jpg) |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzazione Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupvsup-22"></a>DXGI_FORMAT_X32_TYPELESS_G8X24_UINT<sup>V</sup> (22)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzazione Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a>DXGI_FORMAT_R10G10B10A2_TYPELESS<sup>PCS</sup> (23)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a>DXGI_FORMAT_R10G10B10A2_UNORM<sup>FCS</sup> (24)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | ![necessario](images/letter-r.jpg) |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | ![facoltative](images/letter-o.jpg) |
| Output processore video | ![necessario](images/letter-r.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a>DXGI_FORMAT_R10G10B10A2_UINT<sup>FCS</sup> (25)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | ![necessario](images/letter-r.jpg) |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a>DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM<sup>FCS</sup> (89)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | ![necessario](images/letter-r.jpg) |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![necessario](images/letter-r.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a>DXGI_FORMAT_R11G11B10_FLOAT<sup>FNS</sup> (26)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a>DXGI_FORMAT_R8G8B8A8_TYPELESS<sup>PCS</sup> (27)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a>DXGI_FORMAT_R8G8B8A8_UNORM<sup>FCS</sup> (28)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![necessario](images/letter-r.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzazione Scan-Out | ![necessario](images/letter-r.jpg) |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | ![facoltative](images/letter-o.jpg) |
| Output processore video | ![necessario](images/letter-r.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB<sup>FCS</sup> (29)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | ![necessario](images/letter-r.jpg) |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | ![facoltative](images/letter-o.jpg) |
| Output processore video | ![necessario](images/letter-r.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a>DXGI_FORMAT_R8G8B8A8_UINT<sup>FCS</sup> (30)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | ![necessario](images/letter-r.jpg) |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![necessario](images/letter-r.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a>DXGI_FORMAT_R8G8B8A8_SNORM<sup>FCS</sup> (31)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a>DXGI_FORMAT_R8G8B8A8_SINT<sup>FCS</sup> (32)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| Archivio tipidato UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![necessario](images/letter-r.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a>DXGI_FORMAT_R16G16_TYPELESS<sup>PCS</sup> (33)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a>DXGI_FORMAT_R16G16_FLOAT<sup>FCS</sup> (34)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a>DXGI_FORMAT_R16G16_UNORM<sup>FCS</sup> (35)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a>DXGI_FORMAT_R16G16_UINT<sup>FCS</sup> (36)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | ![necessario](images/letter-r.jpg) |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| Archivio tipidato UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a>DXGI_FORMAT_R16G16_SNORM<sup>FCS</sup> (37)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| Archivio tipidato UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a>DXGI_FORMAT_R16G16_SINT<sup>FCS</sup> (38)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| Archivio tipidato UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a>DXGI_FORMAT_R32_TYPELESS<sup>PCS</sup> (39)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | ![necessario](images/letter-r.jpg) |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a>DXGI_FORMAT_D32_FLOAT<sup>FCS</sup> (40)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | ![necessario](images/letter-r.jpg) |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a>DXGI_FORMAT_R32_FLOAT<sup>FCS</sup> (41)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | ![necessario](images/letter-r.jpg) |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| Archivio tipidato UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![necessario](images/letter-r.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | ![necessario](images/letter-r.jpg) |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a>DXGI_FORMAT_R32_UINT<sup>FCS</sup> (42)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer di output del flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | ![necessario](images/letter-r.jpg) |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| Archivio tipidato UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![necessario](images/letter-r.jpg) |
| Aggiunta atomica UAV | ![necessario](images/letter-r.jpg) |
| Operazioni bit per bit atomiche UAV | ![necessario](images/letter-r.jpg) |
| UAV Atomic Cmp&Store/Cmp&Exch | ![necessario](images/letter-r.jpg) |
| UAV Atomic Exchange | ![necessario](images/letter-r.jpg) |
| Min/Max con firma atomica UAV | ![necessario](images/letter-r.jpg) |
| UAV Atomic Unsigned Min/Max | ![necessario](images/letter-r.jpg) |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a>DXGI_FORMAT_R32_SINT<sup>FCS</sup> (43)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| Archivio tipidato UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![necessario](images/letter-r.jpg) |
| Aggiunta atomica UAV | ![necessario](images/letter-r.jpg) |
| Operazioni bit per bit atomiche UAV | ![necessario](images/letter-r.jpg) |
| UAV Atomic Cmp&Store/Cmp&Exch | ![necessario](images/letter-r.jpg) |
| UAV Atomic Exchange | ![necessario](images/letter-r.jpg) |
| Min/Max con firma atomica UAV | ![necessario](images/letter-r.jpg) |
| UAV Atomic Unsigned Min/Max | ![necessario](images/letter-r.jpg) |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r24g8_typelesssupvsup-44"></a>DXGI_FORMAT_R24G8_TYPELESS<sup>V</sup> (44)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupvsup-45"></a>DXGI_FORMAT_D24_UNORM_S8_UINT<sup>V</sup> (45)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | ![necessario](images/letter-r.jpg) |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupvsup-46"></a>DXGI_FORMAT_R24_UNORM_X8_TYPELESS<sup>V</sup> (46)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | ![necessario](images/letter-r.jpg) |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupvsup-47"></a>DXGI_FORMAT_X24_TYPELESS_G8_UINT<sup>V</sup> (47)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzazione Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a>DXGI_FORMAT_R8G8_TYPELESS<sup>PCS</sup> (48)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzazione Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a>DXGI_FORMAT_R8G8_UNORM<sup>FCS</sup> (49)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a>DXGI_FORMAT_R8G8_UINT<sup>FCS</sup> (50)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | ![necessario](images/letter-r.jpg) |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| Archivio tipidato UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a>DXGI_FORMAT_R8G8_SNORM<sup>FCS</sup> (51)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| Archivio tipidato UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a>DXGI_FORMAT_R8G8_SINT<sup>FCS</sup> (52)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a>DXGI_FORMAT_R16_TYPELESS<sup>PCS</sup> (53)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a>DXGI_FORMAT_R16_FLOAT<sup>FCS</sup> (54)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![necessario](images/letter-r.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a>DXGI_FORMAT_D16_UNORM<sup>FCS</sup> (55)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | ![necessario](images/letter-r.jpg) |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a>DXGI_FORMAT_R16_UNORM<sup>FCS</sup> (56)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | ![necessario](images/letter-r.jpg) |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| Archivio tipidato UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a>DXGI_FORMAT_R16_UINT<sup>FCS</sup> (57)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | ![necessario](images/letter-r.jpg) |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| Archivio tipidato UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![necessario](images/letter-r.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a>DXGI_FORMAT_R16_SNORM<sup>FCS</sup> (58)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| Archivio tipidato UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a>DXGI_FORMAT_R16_SINT<sup>FCS</sup> (59)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| Archivio tipidato UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![necessario](images/letter-r.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a>DXGI_FORMAT_R8_TYPELESS<sup>PCS</sup> (60)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a>DXGI_FORMAT_R8_UNORM<sup>FCS</sup> (61)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![necessario](images/letter-r.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a>DXGI_FORMAT_R8_UINT<sup>FCS</sup> (62)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | ![necessario](images/letter-r.jpg) |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| Archivio tipidato UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![necessario](images/letter-r.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a>DXGI_FORMAT_R8_SNORM<sup>FCS</sup> (63)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzazione Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a>DXGI_FORMAT_R8_SINT<sup>FCS</sup> (64)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![necessario](images/letter-r.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a>DXGI_FORMAT_A8_UNORM<sup>FNS</sup> (65)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a>DXGI_FORMAT_R9G9B9E5_SHAREDEXP<sup>FNC</sup> (67)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a>DXGI_FORMAT_R8G8_B8G8_UNORM<sup>FNC</sup> (68)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a>DXGI_FORMAT_G8R8_G8B8_UNORM<sup>FNC</sup> (69)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a>DXGI_FORMAT_BC1_TYPELESS<sup>PCC</sup> (70)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc1_unorm-supfccsup-71"></a>DXGI_FORMAT_BC1_UNORM <sup>FCC</sup> (71)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc1_unorm_srgb-supfccsup-72"></a>DXGI_FORMAT_BC1_UNORM_SRGB <sup>FCC</sup> (72)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a>DXGI_FORMAT_BC2_TYPELESS<sup>PCC</sup> (73)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_unorm-supfccsup-74"></a>DXGI_FORMAT_BC2_UNORM <sup>FCC</sup> (74)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_unorm_srgb-supfccsup-75"></a>DXGI_FORMAT_BC2_UNORM_SRGB <sup>FCC</sup> (75)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a>DXGI_FORMAT_BC3_TYPELESS<sup>PCC</sup> (76)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_unorm-supfccsup-77"></a>DXGI_FORMAT_BC3_UNORM <sup>FCC</sup> (77)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_unorm_srgb-supfccsup-78"></a>DXGI_FORMAT_BC3_UNORM_SRGB <sup>FCC</sup> (78)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzazione Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a>DXGI_FORMAT_BC4_TYPELESS<sup>PCC</sup> (79)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_unorm-supfccsup-80"></a>DXGI_FORMAT_BC4_UNORM <sup>FCC</sup> (80)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_snorm-supfccsup-81"></a>DXGI_FORMAT_BC4_SNORM <sup>FCC</sup> (81)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a>DXGI_FORMAT_BC5_TYPELESS<sup>PCC</sup> (82)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_unorm-supfccsup-83"></a>DXGI_FORMAT_BC5_UNORM <sup>FCC</sup> (83)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_snorm-supfccsup-84"></a>DXGI_FORMAT_BC5_SNORM <sup>FCC</sup> (84)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a>DXGI_FORMAT_B5G6R5_UNORM<sup>FNS</sup> (85)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![facoltative](images/letter-o.jpg) |
| Buffer dei vertici dell'assembler di input | ![facoltative](images/letter-o.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | ![facoltative](images/letter-o.jpg) |
| Archivio tipidato UAV | ![facoltative](images/letter-o.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Altro numero multicampionamento RT | ![necessario](images/letter-r.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a>DXGI_FORMAT_B5G5R5A1_UNORM<sup>FNS</sup> (86)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![facoltative](images/letter-o.jpg) |
| Buffer dei vertici dell'assembler di input | ![facoltative](images/letter-o.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![facoltative](images/letter-o.jpg) |
| RenderTarget | ![facoltative](images/letter-o.jpg) |
| Blendable RenderTarget | ![facoltative](images/letter-o.jpg) |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | ![facoltative](images/letter-o.jpg) |
| Archivio tipidato UAV | ![facoltative](images/letter-o.jpg) |
| Caricamento tipiato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![facoltative](images/letter-o.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a>DXGI_FORMAT_B8G8R8A8_TYPELESS<sup>PCS</sup> (90)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a>DXGI_FORMAT_B8G8R8A8_UNORM<sup>FCS</sup> (87)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzazione Scan-Out | ![necessario](images/letter-r.jpg) |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | ![facoltative](images/letter-o.jpg) |
| Output processore video | ![necessario](images/letter-r.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a>DXGI_FORMAT_B8G8R8A8_UNORM_SRGB<sup>FCS</sup> (91)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzazione Scan-Out | ![necessario](images/letter-r.jpg) |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | ![facoltative](images/letter-o.jpg) |
| Output processore video | ![necessario](images/letter-r.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a>DXGI_FORMAT_B8G8R8X8_TYPELESS<sup>PCS</sup> (92)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a>DXGI_FORMAT_B8G8R8X8_UNORM<sup>FCS</sup> (88)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![facoltative](images/letter-o.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a>DXGI_FORMAT_B8G8R8X8_UNORM_SRGB<sup>FCS</sup> (93)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![necessario](images/letter-r.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_typelesssuppccsup-94"></a>DXGI_FORMAT_BC6H_TYPELESS<sup>PCC</sup> (94)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_uf16-supfccsup-95"></a>DXGI_FORMAT_BC6H_UF16 <sup>FCC</sup> (95)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_sf16-supfccsup-96"></a>DXGI_FORMAT_BC6H_SF16 <sup>FCC</sup> (96)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_typelesssuppccsup-97"></a>DXGI_FORMAT_BC7_TYPELESS<sup>PCC</sup> (97)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_unorm-supfccsup-98"></a>DXGI_FORMAT_BC7_UNORM <sup>FCC</sup> (98)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_unorm_srgb-supfccsup-99"></a>DXGI_FORMAT_BC7_UNORM_SRGB <sup>FCC</sup> (99)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzazione Scan-Out | \- |
| Cast all'interno del layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | ![necessario](images/letter-r.jpg) |

## <a name="dxgi_format_ayuvsupvsup-100"></a>DXGI_FORMAT_AYUV<sup>V</sup> (100)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzazione Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | ![facoltative](images/letter-o.jpg) |
| Input processore video | ![necessario](images/letter-r.jpg) |
| Output processore video | ![facoltative](images/letter-o.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_y410supvsup-101"></a>DXGI_FORMAT_Y410<sup>V</sup> (101)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzazione Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | ![facoltative](images/letter-o.jpg) |
| Input processore video | ![facoltative](images/letter-o.jpg) |
| Output processore video | ![facoltative](images/letter-o.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_y416supvsup-102"></a>DXGI_FORMAT_Y416<sup>V</sup> (102)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | ![facoltative](images/letter-o.jpg) |
| Input processore video | ![facoltative](images/letter-o.jpg) |
| Output processore video | ![facoltative](images/letter-o.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_nv12supvsup-103"></a>DXGI_FORMAT_NV12<sup>V</sup> (103)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| Archivio tipidato UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | ![necessario](images/letter-r.jpg) |
| Input processore video | ![necessario](images/letter-r.jpg) |
| Output del processore video | ![necessario](images/letter-r.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_p010supvsup-104"></a>DXGI_FORMAT_P010<sup>V</sup> (104)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| Archivio tipidato UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | ![facoltative](images/letter-o.jpg) |
| Input processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![facoltative](images/letter-o.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_p016supvsup-105"></a>DXGI_FORMAT_P016<sup>V</sup> (105)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| Archivio tipidato UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | ![facoltative](images/letter-o.jpg) |
| Input processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![facoltative](images/letter-o.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a>DXGI_FORMAT_420_OPAQUE<sup>V</sup> (106)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | \- |
| Archivio tipidato UAV | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzazione Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | ![necessario](images/letter-r.jpg) |
| Input processore video | ![necessario](images/letter-r.jpg) |
| Output processore video | ![necessario](images/letter-r.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a>DXGI_FORMAT_YUY2<sup>V</sup> (107)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | ![necessario](images/letter-r.jpg) |
| UAV Typed Store | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzazione Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | ![facoltative](images/letter-o.jpg) |
| Input processore video | ![necessario](images/letter-r.jpg) |
| Output processore video | ![facoltative](images/letter-o.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_y210supvsup-108"></a>DXGI_FORMAT_Y210<sup>V</sup> (108)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| Archivio tipidato UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | ![facoltative](images/letter-o.jpg) |
| Input processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![facoltative](images/letter-o.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_y216supvsup-109"></a>DXGI_FORMAT_Y216<sup>V</sup> (109)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| Archivio tipidato UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni atomiche bit per bit UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | ![facoltative](images/letter-o.jpg) |
| Input processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![facoltative](images/letter-o.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_nv11supvsup-110"></a>DXGI_FORMAT_NV11<sup>V</sup> (110)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4_c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| Blendable RenderTarget | ![necessario](images/letter-r.jpg) |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV e SRV strutturati | \- |
| UAV tipi di dati | ![necessario](images/letter-r.jpg) |
| Archivio tipidato UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con firma atomica UAV | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | ![facoltative](images/letter-o.jpg) |
| Input processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![facoltative](images/letter-o.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_ai44supvsup-111"></a>DXGI_FORMAT_AI44<sup>V</sup> (111)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output di Operazioni per la logica di fusione | \- |
| Destinazione profondità/stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | ![necessario](images/letter-r.jpg) |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_ia44supvsup-112"></a>DXGI_FORMAT_IA44<sup>V</sup> (112)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | ![necessario](images/letter-r.jpg) |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_p8supvsup-113"></a>DXGI_FORMAT_P8<sup>V</sup> (113)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | ![necessario](images/letter-r.jpg) |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a>DXGI_FORMAT_A8P8<sup>V</sup> (114)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Shader sample_c (filtro di confronto) | \- |
| Esempio di shader (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader gather4_c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Profondità/Destinazione stencil | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipivato | \- |
| UAV Typed Store | \- |
| Caricamento tipiato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Min/Max con segno atomico UAV | \- |
| Numero minimo/massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | ![necessario](images/letter-r.jpg) |
| Output processore video | \- |
| Risorsa condivisa | \- |
| BackBuffer di cui è possibile eseguire il cast anche completamente tipizzata | \- |
| Risorsa affiancata | \- |

## <a name="format-notes"></a>Formattare le note

Lo scopo del formato può cambiare da un livello di funzionalità hardware a quello successivo.

<dl> <dt>

<sup>L:</sup> formato senza tipi
</dt> <dt>

<sup>PCS:</sup> layout parzialmente tipizzabile, di cui è possibile eseguire il cast e semplice
</dt> <dt>

 <sup>FCS:</sup> layout completamente tipizzabile, di cui è possibile eseguire il cast e semplice
</dt> <dt>

<sup>FNS:</sup> layout completo, non di cui è possibile eseguire il cast e semplice
</dt> <dt>

<sup>PCC:</sup> layout parzialmente tipizzato, di cui è possibile eseguire il cast e complesso
</dt> <dt>

 <sup>FCC:</sup> layout completamente tipizzato, di cui è possibile eseguire il cast e complesso
</dt> <dt>

<sup>FNC:</sup> layout completamente tipizzato, non di cui è possibile eseguire il cast e complesso
</dt> <dt>

<sup>V:</sup> formato video
</dt> </dl>

## <a name="dxgi_format_related-topics"></a>DXGI_FORMAT_Related seguenti

[Livelli di funzionalità hardware D3D12](../direct3d12/hardware-feature-levels.md)

[Guida di programmazione per DXGI](dx-graphics-dxgi-overviews.md)
