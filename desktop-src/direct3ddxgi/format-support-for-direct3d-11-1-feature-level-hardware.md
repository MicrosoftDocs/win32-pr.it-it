---
description: Questa sezione specifica i formati ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valori) supportati nell'hardware del livello di funzionalità Direct3D 11,1.
ms.assetid: 90EADE0C-A984-4993-A3F8-D045C535DE64
title: Supporto del formato per l'hardware a livello di funzionalità 11.1 di Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 999228224ebd88c234f46eaa719275fb6cf9bce8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104557207"
---
# <a name="format-support-for-direct3d-feature-level-111-hardware"></a>Supporto del formato per l'hardware a livello di funzionalità 11.1 di Direct3D

Questa sezione specifica i formati ([_* DXGI_FORMAT_* * _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valori) supportati nell'hardware a livello di funzionalità Direct3D 11,1.

La tabella riepiloga il supporto della funzionalità, usando la chiave seguente.

| Simbolo                            | Descrizione                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| _ *-**                             | Non consentito o non disponibile.                                                  |
| ![necessario](images/letter-r.jpg)  | Il supporto hardware è obbligatorio.                                                 |
| ![facoltative](images/letter-o.jpg)  | Supporto hardware facoltativo. il formato potrebbe essere accelerato o meno. |
| ![dipendenti](images/letter-d.jpg) | Obbligatorio se è supportata la funzionalità facoltativa correlata.                            |

Questo argomento contiene una sezione per formato. Una *destinazione* del formato (le tabelle contengono una riga per destinazione) può essere un tipo di risorsa, una funzione intrinseca HLSL o una particolare funzionalità che dipende da un particolare formato.

Per verificare a livello di codice il supporto del formato in D3D11 e D3D12, vedere [controllo della funzionalità hardware](checking-hardware-feature-support.md).

> [!NOTE] 
> Il numero di formati è prevalentemente, ma non tutti, in ordine numerico crescente &mdash; alcuni sono fuori dall'ordine numerico ed elencati insieme ad altri formati pertinenti. Si noti anche che il *tipo* in un nome di formato può indicare *parzialmente* tipizzato e non esclusivamente senza tipo (fare riferimento alla sezione [Note sul formato](#format-notes) alla fine dell'argomento).

## <a name="dxgi_format_unknownsuplsup-0"></a>DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 0 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | ![necessario](images/letter-r.jpg) |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a>DXGI_FORMAT_R32G32B32A32 \_ <sup>PC</sup> non con tipi (1)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a>DXGI_FORMAT_R32G32B32A32 \_ float<sup>FCS</sup> (2)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![facoltative](images/letter-o.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a>DXGI_FORMAT_R32G32B32A32 \_ uint<sup>FCS</sup> (3)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | ![necessario](images/letter-r.jpg) |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![facoltative](images/letter-o.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a>DXGI_FORMAT_R32G32B32A32 \_ Sint<sup>FCS</sup> (4)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![facoltative](images/letter-o.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a>DXGI_FORMAT_R32G32B32 i \_ <sup>PC</sup> con tipi (5)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 96 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a>DXGI_FORMAT_R32G32B32 \_ float<sup>FCS</sup> (6)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 96 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![facoltative](images/letter-o.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![facoltative](images/letter-o.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![facoltative](images/letter-o.jpg) |
| RenderTarget | ![facoltative](images/letter-o.jpg) |
| RenderTarget blendable | ![dipendenti](images/letter-d.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![dipendenti](images/letter-d.jpg) |
| RenderTarget multisample 8x | ![dipendenti](images/letter-d.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a>DXGI_FORMAT_R32G32B32 \_ uint<sup>FCS</sup> (7)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 96 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![facoltative](images/letter-o.jpg) |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | ![necessario](images/letter-r.jpg) |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![dipendenti](images/letter-d.jpg) |
| RenderTarget multisample 8x | ![dipendenti](images/letter-d.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a>DXGI_FORMAT_R32G32B32 \_ Sint<sup>FCS</sup> (8)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 96 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![facoltative](images/letter-o.jpg) |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![dipendenti](images/letter-d.jpg) |
| RenderTarget multisample 8x | ![dipendenti](images/letter-d.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a>DXGI_FORMAT_R16G16B16A16 \_ <sup>PC</sup> non con tipi (9)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a>DXGI_FORMAT_R16G16B16A16 \_ float<sup>FCS</sup> (10)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | ![necessario](images/letter-r.jpg) |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![necessario](images/letter-r.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a>DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FCS</sup> (11)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a>DXGI_FORMAT_R16G16B16A16 \_ uint<sup>FCS</sup> (12)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | ![necessario](images/letter-r.jpg) |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a>DXGI_FORMAT_R16G16B16A16 \_ russare<sup>FCS</sup> (13)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a>DXGI_FORMAT_R16G16B16A16 \_ Sint<sup>FCS</sup> (14)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a>DXGI_FORMAT_R32G32 \_ <sup>PC</sup> non con tipi (15)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a>DXGI_FORMAT_R32G32 \_ float<sup>FCS</sup> (16)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a>DXGI_FORMAT_R32G32 \_ uint<sup>FCS</sup> (17)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | ![necessario](images/letter-r.jpg) |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a>DXGI_FORMAT_R32G32 \_ Sint<sup>FCS</sup> (18)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a>DXGI_FORMAT_R32G8X24 i \_ <sup>PC</sup> non con tipi (19)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfcssup-20"></a>DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup>FCS</sup> (20)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | ![necessario](images/letter-r.jpg) |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfcssup-21"></a>DXGI_FORMAT_R32 \_ float \_ con \_ tipo float<sup></sup> X8X24 (21)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | ![necessario](images/letter-r.jpg) |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfcssup-22"></a>G8X24 con tipo di DXGI_FORMAT_X32 \_ \_ \_ uint<sup>FCS</sup> (22)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a>DXGI_FORMAT_R10G10B10A2 \_ <sup>PC</sup> non con tipi (23)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a>DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FCS</sup> (24)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | ![necessario](images/letter-r.jpg) |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![necessario](images/letter-r.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a>DXGI_FORMAT_R10G10B10A2 \_ uint<sup>FCS</sup> (25)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | ![necessario](images/letter-r.jpg) |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a>DXGI_FORMAT_R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM<sup>FCS</sup> (89)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | ![necessario](images/letter-r.jpg) |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![necessario](images/letter-r.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a>DXGI_FORMAT_R11G11B10 \_ float<sup>FNS</sup> (26)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a>DXGI_FORMAT_R8G8B8A8 \_ <sup>PC</sup> non con tipi (27)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a>DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FCS</sup> (28)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | ![necessario](images/letter-r.jpg) |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![necessario](images/letter-r.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a>DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ sRGB<sup>FCS</sup> (29)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | ![necessario](images/letter-r.jpg) |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![necessario](images/letter-r.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a>DXGI_FORMAT_R8G8B8A8 \_ uint<sup>FCS</sup> (30)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | ![necessario](images/letter-r.jpg) |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a>DXGI_FORMAT_R8G8B8A8 \_ russo<sup>FCS</sup> (31)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a>DXGI_FORMAT_R8G8B8A8 \_ Sint<sup>FCS</sup> (32)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a>DXGI_FORMAT_R16G16 \_ <sup>PC</sup> non con tipi (33)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a>DXGI_FORMAT_R16G16 \_ float<sup>FCS</sup> (34)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a>DXGI_FORMAT_R16G16 \_ UNORM<sup>FCS</sup> (35)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a>DXGI_FORMAT_R16G16 \_ uint<sup>FCS</sup> (36)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | ![necessario](images/letter-r.jpg) |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a>DXGI_FORMAT_R16G16 \_ russo<sup>FCS</sup> (37)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a>DXGI_FORMAT_R16G16 \_ Sint<sup>FCS</sup> (38)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a>DXGI_FORMAT_R32 \_ <sup>PC</sup> non con tipi (39)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | ![necessario](images/letter-r.jpg) |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a>DXGI_FORMAT_D32 \_ float<sup>FCS</sup> (40)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | ![necessario](images/letter-r.jpg) |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a>DXGI_FORMAT_R32 \_ float<sup>FCS</sup> (41)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | ![necessario](images/letter-r.jpg) |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![necessario](images/letter-r.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | ![necessario](images/letter-r.jpg) |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a>DXGI_FORMAT_R32 \_ uint<sup>FCS</sup> (42)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | ![necessario](images/letter-r.jpg) |
| Buffer output flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | ![necessario](images/letter-r.jpg) |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![necessario](images/letter-r.jpg) |
| Aggiunta atomica UAV | ![necessario](images/letter-r.jpg) |
| Operazioni bit per bit atomici UAV | ![necessario](images/letter-r.jpg) |
| UAV Atomic CMP&Store/CMP&Exch | ![necessario](images/letter-r.jpg) |
| Scambio atomico UAV | ![necessario](images/letter-r.jpg) |
| Min/max con segno atomico UAV | ![necessario](images/letter-r.jpg) |
| Min/max senza segno UAV atomico | ![necessario](images/letter-r.jpg) |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a>DXGI_FORMAT_R32 \_ Sint<sup>FCS</sup> (43)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | ![necessario](images/letter-r.jpg) |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![necessario](images/letter-r.jpg) |
| Aggiunta atomica UAV | ![necessario](images/letter-r.jpg) |
| Operazioni bit per bit atomici UAV | ![necessario](images/letter-r.jpg) |
| UAV Atomic CMP&Store/CMP&Exch | ![necessario](images/letter-r.jpg) |
| Scambio atomico UAV | ![necessario](images/letter-r.jpg) |
| Min/max con segno atomico UAV | ![necessario](images/letter-r.jpg) |
| Min/max senza segno UAV atomico | ![necessario](images/letter-r.jpg) |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a>DXGI_FORMAT_R24G8 \_ <sup>PC</sup> non con tipi (44)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfcssup-45"></a>DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FCS</sup> (45)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | ![necessario](images/letter-r.jpg) |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfcssup-46"></a>DXGI_FORMAT_R24 \_ UNORM \_ X8 con \_ tipo<sup>FCS</sup> (46)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | ![necessario](images/letter-r.jpg) |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfcssup-47"></a>DXGI_FORMAT_X24 \_ tipo \_ G8 \_ UINT<sup>FCS</sup> (47)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a>DXGI_FORMAT_R8G8 \_ <sup>PC</sup> non con tipi (48)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a>DXGI_FORMAT_R8G8 \_ UNORM<sup>FCS</sup> (49)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a>DXGI_FORMAT_R8G8 \_ uint<sup>FCS</sup> (50)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | ![necessario](images/letter-r.jpg) |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a>DXGI_FORMAT_R8G8 \_ russo<sup>FCS</sup> (51)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a>DXGI_FORMAT_R8G8 \_ Sint<sup>FCS</sup> (52)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a>DXGI_FORMAT_R16 \_ <sup>PC</sup> non con tipi (53)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a>DXGI_FORMAT_R16 \_ float<sup>FCS</sup> (54)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a>DXGI_FORMAT_D16 \_ UNORM<sup>FCS</sup> (55)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | ![necessario](images/letter-r.jpg) |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a>DXGI_FORMAT_R16 \_ UNORM<sup>FCS</sup> (56)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | ![necessario](images/letter-r.jpg) |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | ![necessario](images/letter-r.jpg) |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a>DXGI_FORMAT_R16 \_ uint<sup>FCS</sup> (57)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | ![necessario](images/letter-r.jpg) |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | ![necessario](images/letter-r.jpg) |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a>DXGI_FORMAT_R16 \_ russo<sup>FCS</sup> (58)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a>DXGI_FORMAT_R16 \_ Sint<sup>FCS</sup> (59)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a>DXGI_FORMAT_R8 \_ <sup>PC</sup> non con tipi (60)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a>DXGI_FORMAT_R8 \_ UNORM<sup>FCS</sup> (61)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a>DXGI_FORMAT_R8 \_ uint<sup>FCS</sup> (62)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | ![necessario](images/letter-r.jpg) |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a>DXGI_FORMAT_R8 \_ russo<sup>FCS</sup> (63)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a>DXGI_FORMAT_R8 \_ Sint<sup>FCS</sup> (64)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a>DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a>DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a>DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a>DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a>DXGI_FORMAT_BC1 \_ <sup>PCC</sup> non tipizzato (70)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_bc1_unorm-supfccsup-71"></a>DXGI_FORMAT_BC1 \_ <sup>FCC</sup> UNORM (71)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_bc1_unorm_srgb-supfccsup-72"></a>DXGI_FORMAT_BC1 \_ UNORM \_ sRGB <sup>FCC</sup> (72)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a>DXGI_FORMAT_BC2 \_ <sup>PCC</sup> non tipizzato (73)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_bc2_unorm-supfccsup-74"></a>DXGI_FORMAT_BC2 \_ <sup>FCC</sup> UNORM (74)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_bc2_unorm_srgb-supfccsup-75"></a>DXGI_FORMAT_BC2 \_ UNORM \_ sRGB <sup>FCC</sup> (75)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a>DXGI_FORMAT_BC3 \_ <sup>PCC</sup> non tipizzato (76)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_bc3_unorm-supfccsup-77"></a>DXGI_FORMAT_BC3 \_ <sup>FCC</sup> UNORM (77)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_bc3_unorm_srgb-supfccsup-78"></a>DXGI_FORMAT_BC3 \_ UNORM \_ sRGB <sup>FCC</sup> (78)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a>DXGI_FORMAT_BC4 \_ <sup>PCC</sup> non tipizzato (79)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_bc4_unorm-supfccsup-80"></a>DXGI_FORMAT_BC4 \_ <sup>FCC</sup> UNORM (80)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_bc4_snorm-supfccsup-81"></a>DXGI_FORMAT_BC4 \_ russare <sup>FCC</sup> (81)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a>DXGI_FORMAT_BC5 \_ <sup>PCC</sup> non tipizzato (82)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_bc5_unorm-supfccsup-83"></a>DXGI_FORMAT_BC5 \_ <sup>FCC</sup> UNORM (83)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_bc5_snorm-supfccsup-84"></a>DXGI_FORMAT_BC5 \_ russare <sup>FCC</sup> (84)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a>DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![facoltative](images/letter-o.jpg) |
| Buffer vertici assembler input | ![facoltative](images/letter-o.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![facoltative](images/letter-o.jpg) |
| Archivio con tipi UAV | ![facoltative](images/letter-o.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![necessario](images/letter-r.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a>DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![facoltative](images/letter-o.jpg) |
| Buffer vertici assembler input | ![facoltative](images/letter-o.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![facoltative](images/letter-o.jpg) |
| RenderTarget | ![facoltative](images/letter-o.jpg) |
| RenderTarget blendable | ![facoltative](images/letter-o.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![facoltative](images/letter-o.jpg) |
| Archivio con tipi UAV | ![facoltative](images/letter-o.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![facoltative](images/letter-o.jpg) |
| RenderTarget multisample 8x | ![facoltative](images/letter-o.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![facoltative](images/letter-o.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a>DXGI_FORMAT_B8G8R8A8 \_ <sup>PC</sup> non con tipi (90)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a>DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FCS</sup> (87)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | ![necessario](images/letter-r.jpg) |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![necessario](images/letter-r.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a>DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ sRGB<sup>FCS</sup> (91)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | ![necessario](images/letter-r.jpg) |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![necessario](images/letter-r.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | ![necessario](images/letter-r.jpg) |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a>DXGI_FORMAT_B8G8R8X8 \_ <sup>PC</sup> non con tipi (92)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a>DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FCS</sup> (88)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![necessario](images/letter-r.jpg) |
| Buffer vertici assembler input | ![necessario](images/letter-r.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![facoltative](images/letter-o.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a>DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ sRGB<sup>FCS</sup> (93)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 8x | ![necessario](images/letter-r.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![necessario](images/letter-r.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_bc6h_typelesssuppccsup-94"></a>DXGI_FORMAT_BC6H \_ <sup>PCC</sup> non tipizzato (94)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_bc6h_uf16-supfccsup-95"></a>DXGI_FORMAT_BC6H \_ <sup>FCC</sup> UF16 (95)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_bc6h_sf16-supfccsup-96"></a>DXGI_FORMAT_BC6H \_ <sup>FCC</sup> SF16 (96)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_bc7_typelesssuppccsup-97"></a>DXGI_FORMAT_BC7 \_ <sup>PCC</sup> non tipizzato (97)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_bc7_unorm-supfccsup-98"></a>DXGI_FORMAT_BC7 \_ <sup>FCC</sup> UNORM (98)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_bc7_unorm_srgb-supfccsup-99"></a>DXGI_FORMAT_BC7 \_ UNORM \_ sRGB <sup>FCC</sup> (99)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 128 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | ![necessario](images/letter-r.jpg) |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="dxgi_format_ayuvsupvsup-100"></a>DXGI_FORMAT_AYUV<sup>V</sup> (100)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![necessario](images/letter-r.jpg) |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | ![facoltative](images/letter-o.jpg) |
| Input del processore video | ![necessario](images/letter-r.jpg) |
| Output del processore video | ![facoltative](images/letter-o.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_y410supvsup-101"></a>DXGI_FORMAT_Y410<sup>V</sup> (101)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | ![facoltative](images/letter-o.jpg) |
| Input del processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![facoltative](images/letter-o.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_y416supvsup-102"></a>DXGI_FORMAT_Y416<sup>V</sup> (102)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 64 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | ![facoltative](images/letter-o.jpg) |
| Input del processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![facoltative](images/letter-o.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_nv12supvsup-103"></a>DXGI_FORMAT_NV12<sup>V</sup> (103)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | ![necessario](images/letter-r.jpg) |
| Input del processore video | ![necessario](images/letter-r.jpg) |
| Output del processore video | ![necessario](images/letter-r.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_p010supvsup-104"></a>DXGI_FORMAT_P010<sup>V</sup> (104)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | ![facoltative](images/letter-o.jpg) |
| Input del processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![facoltative](images/letter-o.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_p016supvsup-105"></a>DXGI_FORMAT_P016<sup>V</sup> (105)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | ![facoltative](images/letter-o.jpg) |
| Input del processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![facoltative](images/letter-o.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a>DXGI_FORMAT_420 \_ opaco<sup>V</sup> (106)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | \- |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | ![necessario](images/letter-r.jpg) |
| Input del processore video | ![necessario](images/letter-r.jpg) |
| Output del processore video | ![necessario](images/letter-r.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a>DXGI_FORMAT_YUY2<sup>V</sup> (107)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | ![facoltative](images/letter-o.jpg) |
| Input del processore video | ![necessario](images/letter-r.jpg) |
| Output del processore video | ![facoltative](images/letter-o.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_y210supvsup-108"></a>DXGI_FORMAT_Y210<sup>V</sup> (108)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | ![facoltative](images/letter-o.jpg) |
| Input del processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![facoltative](images/letter-o.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_y216supvsup-109"></a>DXGI_FORMAT_Y216<sup>V</sup> (109)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 32 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | ![facoltative](images/letter-o.jpg) |
| Input del processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![facoltative](images/letter-o.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_nv11supvsup-110"></a>DXGI_FORMAT_NV11<sup>V</sup> (110)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | ![necessario](images/letter-r.jpg) |
| RenderTarget blendable | ![necessario](images/letter-r.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![necessario](images/letter-r.jpg) |
| Archivio con tipi UAV | ![necessario](images/letter-r.jpg) |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | ![facoltative](images/letter-o.jpg) |
| Input del processore video | ![facoltative](images/letter-o.jpg) |
| Output del processore video | ![facoltative](images/letter-o.jpg) |
| Risorsa condivisa | ![necessario](images/letter-r.jpg) |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_ai44supvsup-111"></a>DXGI_FORMAT_AI44<sup>V</sup> (111)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input del processore video | ![necessario](images/letter-r.jpg) |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_ia44supvsup-112"></a>DXGI_FORMAT_IA44<sup>V</sup> (112)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input del processore video | ![necessario](images/letter-r.jpg) |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_p8supvsup-113"></a>DXGI_FORMAT_P8<sup>V</sup> (113)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 8 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input del processore video | ![necessario](images/letter-r.jpg) |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a>DXGI_FORMAT_A8P8<sup>V</sup> (114)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![facoltative](images/letter-o.jpg) |
| Buffer | \- |
| Buffer vertici assembler input | \- |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | \- |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| LD shader | \- |
| Esempio di shader (qualsiasi filtro) | \- |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Generazione automatica mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | \- |
| Archivio con tipi UAV | \- |
| Caricamento tipizzato UAV | \- |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | \- |
| RenderTarget multisample 8x | \- |
| Altro conteggio multisample RT | \- |
| Risoluzione multicampionamento | \- |
| Carico multicampionamento | \- |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input del processore video | ![necessario](images/letter-r.jpg) |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a>DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115)
| Destinazione | Supporto |
| - | - |
| Bit per elemento (BPE) | 16 |
| Supporto del formato | ![necessario](images/letter-r.jpg) |
| Buffer | ![facoltative](images/letter-o.jpg) |
| Buffer vertici assembler input | ![facoltative](images/letter-o.jpg) |
| Buffer indice input assembler | \- |
| Buffer output flusso | \- |
| Texture1D | ![necessario](images/letter-r.jpg) |
| Texture2D | ![necessario](images/letter-r.jpg) |
| Texture3D | ![necessario](images/letter-r.jpg) |
| TextureCube | ![necessario](images/letter-r.jpg) |
| LD shader | ![necessario](images/letter-r.jpg) |
| Esempio di shader (qualsiasi filtro) | ![necessario](images/letter-r.jpg) |
| Esempio shader \_ c (filtro di confronto) | \- |
| Esempio di shader (filtro mono 1 \_ bit \_ ) | \- |
| Shader gather4 | ![necessario](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| Mipmap | ![necessario](images/letter-r.jpg) |
| Generazione automatica mipmap | ![facoltative](images/letter-o.jpg) |
| RenderTarget | ![facoltative](images/letter-o.jpg) |
| RenderTarget blendable | ![facoltative](images/letter-o.jpg) |
| Operazione logica di Unione output | \- |
| Profondità/stencil di destinazione | \- |
| UAV e SRV non elaborati | \- |
| UAV strutturato e SRV | \- |
| UAV tipizzato | ![facoltative](images/letter-o.jpg) |
| Archivio con tipi UAV | ![facoltative](images/letter-o.jpg) |
| Caricamento tipizzato UAV | ![facoltative](images/letter-o.jpg) |
| Aggiunta atomica UAV | \- |
| Operazioni bit per bit atomici UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Scambio atomico UAV | \- |
| Min/max con segno atomico UAV | \- |
| Min/max senza segno UAV atomico | \- |
| CPU bloccabile | ![necessario](images/letter-r.jpg) |
| RenderTarget multisample 4x | ![facoltative](images/letter-o.jpg) |
| RenderTarget multisample 8x | ![facoltative](images/letter-o.jpg) |
| Altro conteggio multisample RT | ![facoltative](images/letter-o.jpg) |
| Risoluzione multicampionamento | ![necessario](images/letter-r.jpg) |
| Carico multicampionamento | ![facoltative](images/letter-o.jpg) |
| Visualizza Scan-Out | \- |
| Cast nel layout di bit | \- |
| Supporto del decodificatore video | \- |
| Input del processore video | \- |
| Output del processore video | \- |
| Risorsa condivisa | \- |
| Castabile backBuffer anche completamente tipizzato | \- |
| Risorsa affiancata | ![facoltative](images/letter-o.jpg) |

## <a name="format-notes"></a>Note sul formato

Lo scopo del formato può variare da un livello di funzionalità hardware a quello successivo.

<dl> <dt>

<sup>L</sup> : formato non tipizzato
</dt> <dt>

<sup>PC</sup> : layout parzialmente tipizzato, castabile e semplice
</dt> <dt>

 <sup>FCS</sup> : layout completamente tipizzato, castabile e semplice
</dt> <dt>

<sup>FNS</sup> : layout completamente tipizzato, non ristabile e semplice
</dt> <dt>

<sup>PCC</sup> : layout parzialmente tipizzato, castabile e complesso
</dt> <dt>

 <sup>FCC</sup> : layout completamente tipizzato, castabile e complesso
</dt> <dt>

<sup>FNC</sup> : layout completamente tipizzato, non ristabile e complesso
</dt> <dt>

<sup>V</sup> : formato video
</dt> </dl>

## <a name="related-topics"></a>Argomenti correlati

[Livelli di funzionalità hardware D3D12](../direct3d12/hardware-feature-levels.md)

[Guida per programmatori per DXGI](dx-graphics-dxgi-overviews.md)
