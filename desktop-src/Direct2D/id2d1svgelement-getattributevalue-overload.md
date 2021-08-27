---
title: Metodi GetAttributeValue id2D1SvgElement
description: Ottiene un attributo di questo elemento.
ms.assetid: 2f6ca40a-6c78-9c60-c06a-a31f6edf7663
keywords:
- Metodi GetAttributeValue Direct2D
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: cfc85f2af132c52a95f196aa6e0722b4d75ccc9bc8a4b7a1abb992cc581a6f32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076851"
---
# <a name="id2d1svgelementgetattributevalue-methods"></a>Metodi ID2D1SvgElement::GetAttributeValue

Ottiene un attributo di questo elemento.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                     | Descrizione                                                                                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAttributeValue(PCWSTR, FLOAT \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_float))                                         | Ottiene un attributo di questo elemento come float.<br/>                                                                                                    |
| [**GetAttributeValue(PCWSTR, D2D1 \_ COLOR \_ F \* )**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                | Ottiene un attributo di questo elemento come colore.<br/>                                                                                                    |
| [**GetAttributeValue(PCWSTR, REFIID, void \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_refiid_void))                                | Ottiene un attributo di questo elemento come tipo di interfaccia. <br/>                                                                                         |
| [**GetAttributeValue(PCWSTR, D2D1 \_ FILL \_ MODE \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_fill_mode))                              | Ottiene un attributo di questo elemento come modalità di riempimento. Questo metodo può essere usato per ottenere il valore delle proprietà fill-rule o clip-rule.<br/>             |
| [**GetAttributeValue(PCWSTR, ID2D1SvgPaint \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpaint))                              | Ottiene un attributo di questo elemento come disegno. Questo metodo può essere usato per ottenere il valore delle proprietà di riempimento o tratto.<br/>                         |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ LENGTH \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_length))                            | Ottiene un attributo di questo elemento come valore di lunghezza.<br/>                                                                                             |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ DISPLAY \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_display))                            | Ottiene un attributo di questo elemento come valore di visualizzazione. Questo metodo può essere usato per ottenere il valore della proprietà di visualizzazione.<br/>                          |
| [**GetAttributeValue(PCWSTR, D2D1 \_ EXTEND \_ MODE \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_extend_mode))                           | Ottiene un attributo di questo elemento come valore della modalità di estensione. Questo metodo può essere usato per ottenere il valore di un attributo spreadMethod.<br/>                  |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ OVERFLOW \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_overflow))                           | Ottiene un attributo di questo elemento come valore di overflow. Questo metodo può essere usato per ottenere il valore della proprietà di overflow.<br/>                       |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ LINE \_ CAP \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_line_cap))                         | Ottiene un attributo di questo elemento come valore del limite di riga. Questo metodo può essere usato per ottenere il valore della proprietà stroke-linecap.<br/>                  |
| [**GetAttributeValue(PCWSTR, D2D1 \_ MATRIX \_ 3X2 \_ F \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_matrix_3x2_f))                         | Ottiene un attributo di questo elemento come valore di matrice. Questo metodo può essere usato per ottenere il valore di un attributo transform o gradientTransform.<br/>     |
| [**GetAttributeValue(PCWSTR, ID2D1SvgPathData \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpathdata))                           | Ottiene un attributo di questo elemento come dati di percorso. Questo metodo può essere usato per ottenere il valore dell'attributo d in un elemento path.<br/>                   |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ LINE \_ JOIN \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_line_join))                         | Ottiene un attributo di questo elemento come valore di line join. Questo metodo può essere usato per ottenere il valore della proprietà stroke-linejoin.<br/>                |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ UNIT \_ TYPE \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_unit_type))                        | Ottiene un attributo di questo elemento come valore del tipo di unità. Questo metodo può essere usato per ottenere il valore di un attributo gradientUnits o clipPathUnits.<br/>  |
| [**GetAttributeValue(PCWSTR, ID2D1SvgAttribute \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgattribute))                          | Ottiene un attributo di questo elemento.<br/>                                                                                                               |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ VISIBILITY \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_visibility))                        | Ottiene un attributo di questo elemento come valore di visibilità. Questo metodo può essere usato per ottenere il valore della proprietà visibility.<br/>                    |
| [**GetAttributeValue(PCWSTR, ID2D1SvgStrokeDashArray \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgstrokedasharray))                    | Ottiene un attributo di questo elemento come matrice trattino del tratto. Questo metodo può essere usato per ottenere il valore della proprietà stroke-dasharray.<br/>             |
| [**GetAttributeValue(PCWSTR, ID2D1SvgPointCollection \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpointcollection))                    | Ottiene un attributo di questo elemento come punti. Questo metodo può essere usato per ottenere il valore dell'attributo points in un elemento poligono o polilinea.<br/>  |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ PRESERVE ASPECT RATIO \_ \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_preserve_aspect_ratio))           | Ottiene un attributo di questo elemento come valore di mantenimento delle proporzioni. Questo metodo può essere usato per ottenere il valore di un attributo preserveAspectRatio.<br/> |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ ATTRIBUTE \_ POD \_ TYPE, void \* , UINT32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_attribute_pod_type_void_uint32)) | Ottiene un attributo di questo elemento come tipo POD.<br/>                                                                                                 |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ ATTRIBUTE \_ STRING \_ TYPE, PWSTR, UINT32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_color_f))  | Ottiene un attributo di questo elemento come stringa. <br/>                                                                                                  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)
</dt> </dl>

 

