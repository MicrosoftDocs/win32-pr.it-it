---
description: Questa sezione specifica i formati [**(DXGI_FORMAT_)** *](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) supportati nell'hardware Direct3D Feature 10Level9 9.3.
ms.assetid: B2A843D5-6A6B-4180-8B94-D032B1322798
title: Supporto del formato per l'hardware a livello di funzionalità 10Level9 9.3 di Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ad2746ce0d6e277f04783ae7140f3855fa7078e9a50b67d1e52bc827403c4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951281"
---
# <a name="format-support-for-direct3d-feature-10level9-93-hardware"></a>Supporto del formato per l'hardware a livello di funzionalità 10Level9 9.3 di Direct3D

Questa sezione specifica i formati [**(DXGI_FORMAT_)** *](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) supportati nell'hardware Direct3D Feature 10Level9 9.3.

La tabella riepiloga il supporto delle funzionalità, usando la chiave seguente.

| Simbolo                            | Descrizione                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| **-**                             | Non consentito o non disponibile.                                                  |
| ![necessario](images/letter-r.jpg)  | È necessario il supporto hardware.                                                 |
| ![facoltative](images/letter-o.jpg)  | Supporto hardware facoltativo. Il formato può essere accelerato dall'hardware o meno. |
| ![Dipendente](images/letter-d.jpg) | Obbligatorio se è supportata la funzionalità facoltativa correlata.                            |

Questo argomento contiene una sezione per ogni formato. Una destinazione *di formato* (le tabelle contengono una riga per ogni destinazione) può essere un tipo di risorsa, una funzione intrinseca HLSL o una particolare funzionalità che dipende da un formato specifico.

Per verificare a livello di codice il supporto del formato in D3D11 e D3D12, vedere [Controllo del supporto delle funzionalità hardware.](checking-hardware-feature-support.md)

> [!NOTE] 
> I numeri dei formati sono principalmente, ma non tutti, in ordine numerico crescente, alcuni non sono in ordine numerico ed elencati insieme ad &mdash; altri formati rilevanti. Si noti *anche* che senza tipi  in un nome di formato può significare [](#format-notes) parzialmente digitato e non strettamente senza tipi (vedere la sezione Note sul formato alla fine dell'argomento).

## <a name="dxgi_format_unknownsuplsup-0"></a>DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 0 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a>DXGI_FORMAT_R32G32B32A32 \_ <sup>PCS SENZA TIPO</sup> (1)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfnssup-2"></a>DXGI_FORMAT_R32G32B32A32 FLOAT \_ <sup>FNS</sup> (2)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio di shader (solo esempio di punto) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfnssup-3"></a>DXGI_FORMAT_R32G32B32A32 \_ UINT<sup>FNS</sup> (3)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfnssup-4"></a>DXGI_FORMAT_R32G32B32A32 \_ SINT<sup>FNS</sup> (4)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a>DXGI_FORMAT_R32G32B32 \_ <sup>PCS SENZA TIPO</sup> (5)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 96 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32g32b32_floatsupfnssup-6"></a>DXGI_FORMAT_R32G32B32 \_ <sup>FNS</sup> FLOAT (6)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 96 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
| 4x Multisample RenderTarget | ![Dipendente](images/letter-d.jpg) |
| 8x Multisample RenderTarget | ![Dipendente](images/letter-d.jpg) |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32g32b32_uintsupfnssup-7"></a>DXGI_FORMAT_R32G32B32 \_ <sup>FNS</sup> UINT (7)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 96 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
| 4x Multisample RenderTarget | ![Dipendente](images/letter-d.jpg) |
| 8x Multisample RenderTarget | ![Dipendente](images/letter-d.jpg) |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzazione Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32g32b32_sintsupfnssup-8"></a>DXGI_FORMAT_R32G32B32 \_ SINT<sup>FNS</sup> (8)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 96 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
| 4x Multisample RenderTarget | ![Dipendente](images/letter-d.jpg) |
| 8x Multisample RenderTarget | ![Dipendente](images/letter-d.jpg) |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzazione Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a>DXGI_FORMAT_R16G16B16A16 \_ <sup>PCS SENZA TIPO</sup> (9)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfnssup-10"></a>DXGI_FORMAT_R16G16B16A16 FLOAT \_ <sup>FNS</sup> (10)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio di shader (solo esempio di punto) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![facoltative](images/letter-o.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfnssup-11"></a>DXGI_FORMAT_R16G16B16A16 \_ <sup>UNORM FNS</sup> (11)
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
| Esempio shader (solo campione di punti) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfnssup-12"></a>DXGI_FORMAT_R16G16B16A16 \_ UINT<sup>FNS</sup> (12)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfnssup-13"></a>DXGI_FORMAT_R16G16B16A16 \_ SNORM<sup>FNS</sup> (13)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfnssup-14"></a>DXGI_FORMAT_R16G16B16A16 \_ SINT<sup>FNS</sup> (14)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a>DXGI_FORMAT_R32G32 \_ <sup>PCS SENZA TIPO</sup> (15)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32g32_floatsupfnssup-16"></a>DXGI_FORMAT_R32G32 \_ <sup>FNS</sup> FLOAT (16)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio shader (solo campione di punti) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32g32_uintsupfnssup-17"></a>DXGI_FORMAT_R32G32 \_ UINT<sup>FNS</sup> (17)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32g32_sintsupfnssup-18"></a>DXGI_FORMAT_R32G32 \_ SINT<sup>FNS</sup> (18)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a>DXGI_FORMAT_R32G8X24 \_ <sup>PCS SENZA TIPO</sup> (19)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfnssup-20"></a>DXGI_FORMAT_D32 FLOAT \_ \_ S8X24 \_ UINT<sup>FNS</sup> (20)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfnssup-21"></a>DXGI_FORMAT_R32 \_ FNS FLOAT \_ X8X24 \_ SENZA<sup>TIPI</sup> (21)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfnssup-22"></a>DXGI_FORMAT_X32 \_ TYPELESS \_ G8X24 \_ UINT<sup>FNS</sup> (22)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a>DXGI_FORMAT_R10G10B10A2 \_ <sup>PCS SENZA TIPO</sup> (23)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfnssup-24"></a>DXGI_FORMAT_R10G10B10A2 \_ <sup>UNORM FNS</sup> (24)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfnssup-25"></a>DXGI_FORMAT_R10G10B10A2 \_ UINT<sup>FNS</sup> (25)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfnssup-89"></a>DXGI_FORMAT_R10G10B10 \_ XR \_ BIAS \_ A2 \_ UNORM<sup>FNS</sup> (89)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a>DXGI_FORMAT_R11G11B10 \_ <sup>FNS</sup> FLOAT (26)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a>DXGI_FORMAT_R8G8B8A8 \_ <sup>PCS SENZA TIPO</sup> (27)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfnssup-28"></a>DXGI_FORMAT_R8G8B8A8 \_ <sup>UNORM FNS</sup> (28)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio shader (solo campione di punti) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | ![necessario](images/letter-r.jpg) |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![necessario](images/letter-r.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfnssup-29"></a>DXGI_FORMAT_R8G8B8A8 \_ UNRM \_ SRGB<sup>FNS</sup> (29)
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
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio shader (solo campione di punti) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | ![necessario](images/letter-r.jpg) |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![necessario](images/letter-r.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfnssup-30"></a>DXGI_FORMAT_R8G8B8A8 \_ <sup>FNS</sup> UINT (30)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfnssup-31"></a>DXGI_FORMAT_R8G8B8A8 \_ SNORM<sup>FNS</sup> (31)
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
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio shader (solo campione di punti) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfnssup-32"></a>DXGI_FORMAT_R8G8B8A8 \_ SINT<sup>FNS</sup> (32)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a>DXGI_FORMAT_R16G16 \_ <sup>PCS SENZA TIPO</sup> (33)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r16g16_floatsupfnssup-34"></a>DXGI_FORMAT_R16G16 \_ <sup>FNS</sup> FLOAT (34)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio shader (solo campione di punti) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r16g16_unormsupfnssup-35"></a>DXGI_FORMAT_R16G16 \_ <sup>UNORM FNS</sup> (35)
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
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio shader (solo campione di punti) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r16g16_uintsupfnssup-36"></a>DXGI_FORMAT_R16G16 \_ <sup>FNS</sup> UINT (36)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r16g16_snormsupfnssup-37"></a>DXGI_FORMAT_R16G16 \_ SNORM<sup>FNS</sup> (37)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio shader (solo campione di punti) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r16g16_sintsupfnssup-38"></a>DXGI_FORMAT_R16G16 \_ SINT<sup>FNS</sup> (38)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a>DXGI_FORMAT_R32 \_ <sup>PCS SENZA TIPO</sup> (39)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzazione Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_d32_floatsupfnssup-40"></a>DXGI_FORMAT_D32 FLOAT \_ <sup>FNS</sup> (40)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzazione Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32_floatsupfnssup-41"></a>DXGI_FORMAT_R32 FLOAT \_ <sup>FNS</sup> (41)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio di shader (solo esempio di punto) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32_uintsupfnssup-42"></a>DXGI_FORMAT_R32 \_ UINT<sup>FNS</sup> (42)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32_sintsupfnssup-43"></a>DXGI_FORMAT_R32 \_ SINT<sup>FNS</sup> (43)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a>DXGI_FORMAT_R24G8 \_ <sup>PCS SENZA TIPO</sup> (44)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfnssup-45"></a>DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FNS</sup> (45)
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
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
| 4x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfnssup-46"></a>DXGI_FORMAT_R24 \_ UNRM \_ X8 \_ TYPELESS<sup>FNS</sup> (46)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfnssup-47"></a>DXGI_FORMAT_X24 \_ TYPELESS \_ G8 \_ UINT<sup>FNS</sup> (47)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a>DXGI_FORMAT_R8G8 \_ <sup>PCS SENZA TIPO</sup> (48)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r8g8_unormsupfnssup-49"></a>DXGI_FORMAT_R8G8 \_ UNORM<sup>FNS</sup> (49)
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
| Esempio di shader (solo esempio di punto) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r8g8_uintsupfnssup-50"></a>DXGI_FORMAT_R8G8 \_ UINT<sup>FNS</sup> (50)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r8g8_snormsupfnssup-51"></a>DXGI_FORMAT_R8G8 \_ SNORM<sup>FNS</sup> (51)
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
| Esempio di shader (solo esempio di punto) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r8g8_sintsupfnssup-52"></a>DXGI_FORMAT_R8G8 \_ SINT<sup>FNS</sup> (52)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a>DXGI_FORMAT_R16 \_ <sup>PCS SENZA TIPO</sup> (53)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r16_floatsupfnssup-54"></a>DXGI_FORMAT_R16 \_ FLOAT<sup>FNS</sup> (54)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_d16_unormsupfnssup-55"></a>DXGI_FORMAT_D16 \_ <sup>UNORM FNS</sup> (55)
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
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
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
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
| 4x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| Altro numero multicampionamento RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r16_unormsupfnssup-56"></a>DXGI_FORMAT_R16 \_ <sup>UNORM FNS</sup> (56)
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
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio shader (solo campione di punti) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r16_uintsupfnssup-57"></a>DXGI_FORMAT_R16 \_ UINT<sup>FNS</sup> (57)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | ![necessario](images/letter-r.jpg) |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r16_snormsupfnssup-58"></a>DXGI_FORMAT_R16 \_ SNORM<sup>FNS</sup> (58)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r16_sintsupfnssup-59"></a>DXGI_FORMAT_R16 \_ SINT<sup>FNS</sup> (59)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a>DXGI_FORMAT_R8 \_ <sup>PCS SENZA TIPO</sup> (60)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r8_unormsupfnssup-61"></a>DXGI_FORMAT_R8 \_ <sup>UNORM FNS</sup> (61)
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
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio shader (solo campione di punti) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r8_uintsupfnssup-62"></a>DXGI_FORMAT_R8 \_ UINT<sup>FNS</sup> (62)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r8_snormsupfnssup-63"></a>DXGI_FORMAT_R8 \_ SNORM<sup>FNS</sup> (63)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r8_sintsupfnssup-64"></a>DXGI_FORMAT_R8 \_ SINT<sup>FNS</sup> (64)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a>DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65)
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
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio di shader (solo esempio di punto) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a>DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a>DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a>DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a>DXGI_FORMAT_BC1 \_ <sup>PCC SENZA TIPO</sup> (70)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 4 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_bc1_unormsupfncsup-71"></a>DXGI_FORMAT_BC1 \_ UNORM<sup>FNC</sup> (71)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 4 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio di shader (solo esempio di punto) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzazione Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfncsup-72"></a>DXGI_FORMAT_BC1 \_ UNORM \_ SRGB<sup>FNC</sup> (72)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 4 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio di shader (solo esempio di punto) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a>DXGI_FORMAT_BC2 \_ <sup>PCC SENZA TIPO</sup> (73)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_bc2_unormsupfncsup-74"></a>DXGI_FORMAT_BC2 \_ <sup>UNORM FNC</sup> (74)
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
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio shader (solo campione di punti) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfncsup-75"></a>DXGI_FORMAT_BC2 \_ UNORM \_ SRGB<sup>FNC</sup> (75)
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
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio shader (solo campione di punti) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a>DXGI_FORMAT_BC3 \_ <sup>PCC SENZA TIPO</sup> (76)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_bc3_unormsupfncsup-77"></a>DXGI_FORMAT_BC3 \_ UNORM<sup>FNC</sup> (77)
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
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio di shader (solo esempio di punto) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfncsup-78"></a>DXGI_FORMAT_BC3 \_ UNORM \_ SRGB<sup>FNC</sup> (78)
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
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio di shader (solo esempio di punto) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a>DXGI_FORMAT_BC4 \_ <sup>PCC SENZA TIPO</sup> (79)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 4 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_bc4_unormsupfncsup-80"></a>DXGI_FORMAT_BC4 \_ UNORM<sup>FNC</sup> (80)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 4 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_bc4_snormsupfncsup-81"></a>DXGI_FORMAT_BC4 \_ <sup>FNC</sup> SNORM (81)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 4 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a>DXGI_FORMAT_BC5 \_ <sup>PCC SENZA TIPO</sup> (82)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_bc5_unormsupfncsup-83"></a>DXGI_FORMAT_BC5 \_ UNORM<sup>FNC</sup> (83)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_bc5_snormsupfncsup-84"></a>DXGI_FORMAT_BC5 \_ SNORM<sup>FNC</sup> (84)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a>DXGI_FORMAT_B5G6R5 \_ <sup>UNORM FNS</sup> (85)
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
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio shader (solo campione di punti) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a>DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86)
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
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio di shader (solo esempio di punto) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a>DXGI_FORMAT_B8G8R8A8 \_ <sup>PCS SENZA TIPO</sup> (90)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
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
| Risorsa affiancata | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfnssup-87"></a>DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FNS</sup> (87)
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
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio di shader (solo esempio di punto) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | ![necessario](images/letter-r.jpg) |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | ![facoltative](images/letter-o.jpg) |
| Output processore video | ![necessario](images/letter-r.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfnssup-91"></a>DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ SRGB<sup>FNS</sup> (91)
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
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio di shader (solo esempio di punto) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | ![necessario](images/letter-r.jpg) |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | ![facoltative](images/letter-o.jpg) |
| Output processore video | ![necessario](images/letter-r.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a>DXGI_FORMAT_B8G8R8X8 \_ <sup>PCS SENZA TIPO</sup> (92)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | \- |
| Buffer | \- |
| Buffer dei vertici dell'assembler di input | \- |
| Buffer dell'indice dell'assembler di input | \- |
| Buffer di output del flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzazione Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfnssup-88"></a>DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FNS</sup> (88)
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
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio di shader (solo esempio di punto) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | \- |
| Visualizzazione Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | ![facoltative](images/letter-o.jpg) |
| Output processore video | ![facoltative](images/letter-o.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfnssup-93"></a>DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ SRGB<sup>FNS</sup> (93)
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
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio di shader (solo esempio di punto) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![facoltative](images/letter-o.jpg) |
| Other Multisample Count RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | \- |
| Visualizzazione Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | \- |
| Output processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | \- |

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
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Risorsa condivisa | \- |
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
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Risorsa condivisa | \- |
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
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Output del processore video | ![facoltative](images/letter-o.jpg) |
| Risorsa condivisa | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_nv12supvsup-103"></a>DXGI_FORMAT_NV12<sup>V</sup> (103)
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
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Risorsa condivisa | \- |
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
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/ Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Risorsa condivisa | \- |
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
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Risorsa condivisa | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a>DXGI_FORMAT_420 \_ OPAQUE<sup>V</sup> (106)
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
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | ![necessario](images/letter-r.jpg) |
| Input processore video | ![necessario](images/letter-r.jpg) |
| Output del processore video | ![facoltative](images/letter-o.jpg) |
| Risorsa condivisa | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a>DXGI_FORMAT_YUY2<sup>V</sup> (107)
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
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Operazioni bit per bit atomiche UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Risorsa condivisa | \- |
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
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Risorsa condivisa | \- |
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
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Risorsa condivisa | \- |
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
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Risorsa condivisa | \- |
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
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | ![necessario](images/letter-r.jpg) |
| Output processore video | \- |
| Risorsa condivisa | \- |
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
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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
| Esempio di shader (solo esempio di punto) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | ![necessario](images/letter-r.jpg) |
| Output del processore video | \- |
| Risorsa condivisa | \- |
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
| Esempio shader (solo campione di punti) | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Altro numero multicampionamento RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizzare Scan-Out | \- |
| Cast all'interno del layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input processore video | ![necessario](images/letter-r.jpg) |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a>DXGI_FORMAT_B4G4R4A4 \_ <sup>UNORM FNS</sup> (115)
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
| TextureCube | ![necessario](images/letter-r.jpg) |
| Esempio shader (solo campione di punti) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio di \_ shader c (filtro di confronto) | \- |
| Esempio di shader (filtro mono a 1 bit) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![facoltative](images/letter-o.jpg) |
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
| Numero minimo o massimo con segno atomico UAV | \- |
| Numero minimo o massimo senza segno atomico UAV | \- |
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

<sup>FNS:</sup> layout completamente tipizzato, non di cui è possibile eseguire il cast e semplice
</dt> <dt>

<sup>PCC:</sup> layout parzialmente tipizzabile, di cui è possibile eseguire il cast e complesso
</dt> <dt>

 <sup>FCC:</sup> layout completamente tipizzabile, di cui è possibile eseguire il cast e complesso
</dt> <dt>

<sup>FNC:</sup> layout completamente tipizzato, non di cui è possibile eseguire il cast e complesso
</dt> <dt>

<sup>V:</sup> formato video
</dt> </dl>

## <a name="related-topics"></a>Argomenti correlati

[Livelli di funzionalità hardware D3D12](../direct3d12/hardware-feature-levels.md)

[Implementazione di buffer shadow per la funzionalità Direct3D livello 9](/previous-versions/windows/apps/jj262110(v=win.10))

[Mapping di formati legacy](../direct3d10/d3d10-graphics-programming-guide-resources-legacy-formats.md)

[Guida per programmatori per DXGI](dx-graphics-dxgi-overviews.md)
