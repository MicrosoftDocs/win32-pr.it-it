---
title: Metodi GetAttributeValue di ID2D1SvgElement
description: Ottiene un attributo di questo elemento.
ms.assetid: 2f6ca40a-6c78-9c60-c06a-a31f6edf7663
keywords:
- Metodo GetAttributeValue Direct2D
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: 85e31a8efb1e39d47ab3959fc5ecc175336ab7b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047002"
---
# <a name="id2d1svgelementgetattributevalue-methods"></a>Metodi ID2D1SvgElement:: GetAttributeValue

Ottiene un attributo di questo elemento.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                     | Descrizione                                                                                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAttributeValue (PCWSTR, FLOAT \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_float))                                         | Ottiene un attributo di questo elemento come float.<br/>                                                                                                    |
| [**GetAttributeValue (PCWSTR, D2D1 \_ Color \_ F \* )**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                | Ottiene un attributo di questo elemento come colore.<br/>                                                                                                    |
| [**GetAttributeValue (PCWSTR, REFIID, void \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_refiid_void))                                | Ottiene un attributo di questo elemento come tipo di interfaccia. <br/>                                                                                         |
| [**GetAttributeValue (modalità di riempimento PCWSTR, D2D1 \_ \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_fill_mode))                              | Ottiene un attributo di questo elemento come modalità di riempimento. Questo metodo può essere utilizzato per ottenere il valore delle proprietà della regola di riempimento o della regola di ritaglio.<br/>             |
| [**GetAttributeValue (PCWSTR, ID2D1SvgPaint \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpaint))                              | Ottiene un attributo di questo elemento come disegno. Questo metodo può essere utilizzato per ottenere il valore delle proprietà Fill o Stroke.<br/>                         |
| [**GetAttributeValue (PCWSTR, D2D1 \_ - \_ lunghezza SVG \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_length))                            | Ottiene un attributo dell'elemento come valore di lunghezza.<br/>                                                                                             |
| [**GetAttributeValue (PCWSTR, D2D1 \_ SVG \_ display \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_display))                            | Ottiene un attributo dell'elemento come valore di visualizzazione. Questo metodo può essere utilizzato per ottenere il valore della proprietà di visualizzazione.<br/>                          |
| [**GetAttributeValue (PCWSTR, D2D1 \_ Extended \_ mode \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_extend_mode))                           | Ottiene un attributo di questo elemento come valore della modalità di estensione. Questo metodo può essere utilizzato per ottenere il valore di un attributo spreadMethod.<br/>                  |
| [**GetAttributeValue (PCWSTR, D2D1 \_ SVG \_ overflow \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_overflow))                           | Ottiene un attributo dell'elemento come valore di overflow. Questo metodo può essere utilizzato per ottenere il valore della proprietà di overflow.<br/>                       |
| [**GetAttributeValue (PCWSTR, D2D1 \_ di \_ riga \_ SVG \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_line_cap))                         | Ottiene un attributo di questo elemento come valore della terminazione di riga. Questo metodo può essere utilizzato per ottenere il valore della proprietà Stroke-estremità.<br/>                  |
| [**GetAttributeValue (PCWSTR, D2D1 \_ Matrix \_ 3x2 \_ F \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_matrix_3x2_f))                         | Ottiene un attributo dell'elemento come valore della matrice. Questo metodo può essere utilizzato per ottenere il valore di un attributo Transform o gradientTransform.<br/>     |
| [**GetAttributeValue (PCWSTR, ID2D1SvgPathData \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpathdata))                           | Ottiene un attributo dell'elemento come dati del percorso. Questo metodo può essere utilizzato per ottenere il valore dell'attributo d su un elemento Path.<br/>                   |
| [**GetAttributeValue (PCWSTR, D2D1 \_ - \_ aggiunta alla riga SVG \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_line_join))                         | Ottiene un attributo di questo elemento come valore di join di riga. Questo metodo può essere utilizzato per ottenere il valore della proprietà Stroke-LineJoin.<br/>                |
| [**GetAttributeValue (tipo di unità SVG PCWSTR, D2D1 \_ \_ \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_unit_type))                        | Ottiene un attributo dell'elemento come valore del tipo di unità. Questo metodo può essere utilizzato per ottenere il valore di un attributo gradientUnits o clipPathUnits.<br/>  |
| [**GetAttributeValue (PCWSTR, ID2D1SvgAttribute \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgattribute))                          | Ottiene un attributo di questo elemento.<br/>                                                                                                               |
| [**GetAttributeValue (PCWSTR, D2D1 \_ SVG \_ visibility \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_visibility))                        | Ottiene un attributo dell'elemento come valore di visibilità. Questo metodo può essere utilizzato per ottenere il valore della proprietà Visibility.<br/>                    |
| [**GetAttributeValue (PCWSTR, ID2D1SvgStrokeDashArray \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgstrokedasharray))                    | Ottiene un attributo di questo elemento come matrice di trattini del tratto. Questo metodo può essere utilizzato per ottenere il valore della proprietà Stroke-dashArray.<br/>             |
| [**GetAttributeValue (PCWSTR, ID2D1SvgPointCollection \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpointcollection))                    | Ottiene un attributo dell'elemento come Points. Questo metodo può essere utilizzato per ottenere il valore dell'attributo Points su un elemento Polygon o polilinea.<br/>  |
| [**GetAttributeValue (PCWSTR, D2D1 \_ SVG \_ Preserve \_ \_ proporzione \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_preserve_aspect_ratio))           | Ottiene un attributo di questo elemento come valore di proporzioni di conservazione. Questo metodo può essere utilizzato per ottenere il valore di un attributo preserveAspectRatio.<br/> |
| [**GetAttributeValue (PCWSTR, D2D1 \_ SVG \_ Attribute \_ \_ Type, void \* , UInt32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_attribute_pod_type_void_uint32)) | Ottiene un attributo di questo elemento come tipo POD.<br/>                                                                                                 |
| [**GetAttributeValue (PCWSTR, D2D1 \_ SVG \_ Attribute \_ stringa \_ Type, PWSTR, UInt32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_color_f))  | Ottiene un attributo di questo elemento sotto forma di stringa. <br/>                                                                                                  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)
</dt> </dl>

 

