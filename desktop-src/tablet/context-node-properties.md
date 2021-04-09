---
description: Definisce gli identificatori univoci globali (GUID) per le proprietà di un IContextNode.
ms.assetid: 14992253-c384-43c1-9465-e015ea2348db
title: Proprietà del nodo di contesto (Iaguid. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_CNP_ALIGNMENTLEVEL
- GUID_CNP_ASCENDERS
- GUID_CNP_BASELINE
- GUID_CNP_CONFIDENCELEVEL
- GUID_CNP_CUSTOMRECOGNIZERID
- GUID_CNP_DESCENDERS
- GUID_CNP_MIDLINE
- GUID_CNP_NODEDATA
- GUID_CNP_RECOGNIZEDSTRING
- GUID_CNP_ROTATEDBOUNDINGBOX
- GUID_CNP_SEMANTICTYPE
- GUID_CNP_SHAPENAME
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 8eb1034516c62e2121f835951d1f04db5710d275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878414"
---
# <a name="context-node-properties"></a>Proprietà del nodo di contesto

Definisce gli identificatori univoci globali (GUID) per le proprietà di un [**IContextNode**](icontextnode.md).

Nella tabella seguente vengono descritte le informazioni a cui fa riferimento ogni costante.



| Costante                                                                                                                                                                                                 | Descrizione                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_CNP_ALIGNMENTLEVEL"></span><span id="guid_cnp_alignmentlevel"></span><dl> <dt>**GUID \_ CNP \_ ALIGNMENTLEVEL**</dt> </dl>             | Livello di allineamento di un paragrafo.<br/>                                                                                                               |
| <span id="GUID_CNP_ASCENDERS"></span><span id="guid_cnp_ascenders"></span><dl> <dt>**GUID \_ CNP \_ ascenders**</dt> </dl>                            | Oggetto ascendente di una parola di input penna.<br/>                                                                                                                     |
| <span id="GUID_CNP_BASELINE"></span><span id="guid_cnp_baseline"></span><dl> <dt>**\_linea di \_ base CNP GUID**</dt> </dl>                               | Linea di base di una parola di input penna.<br/>                                                                                                                      |
| <span id="GUID_CNP_CONFIDENCELEVEL"></span><span id="guid_cnp_confidencelevel"></span><dl> <dt>**GUID \_ CNP \_ CONFIDENCELEVEL**</dt> </dl>          | Livello di confidenza nei risultati del riconoscimento.<br/>                                                                                                  |
| <span id="GUID_CNP_CUSTOMRECOGNIZERID"></span><span id="guid_cnp_customrecognizerid"></span><dl> <dt>**GUID \_ CNP \_ CUSTOMRECOGNIZERID**</dt> </dl> | Identificatore del riconoscimento input penna personalizzato per un nodo di riconoscimento personalizzato.<br/>                                                                         |
| <span id="GUID_CNP_DESCENDERS"></span><span id="guid_cnp_descenders"></span><dl> <dt>**\_CNP \_ DISCENDEnti GUID**</dt> </dl>                         | Discendenti di una parola di input penna.<br/>                                                                                                                    |
| <span id="GUID_CNP_MIDLINE"></span><span id="guid_cnp_midline"></span><dl> <dt>**linea \_ media CNP GUID \_**</dt> </dl>                                  | Linea media di una parola di input penna.<br/>                                                                                                                       |
| <span id="GUID_CNP_NODEDATA"></span><span id="guid_cnp_nodedata"></span><dl> <dt>**GUID \_ CNP \_ NODEDATA**</dt> </dl>                               | Dati dell'immagine o dati di testo di un'immagine o di una parola di testo.<br/>                                                                                           |
| <span id="GUID_CNP_RECOGNIZEDSTRING"></span><span id="guid_cnp_recognizedstring"></span><dl> <dt>**GUID \_ CNP \_ RECOGNIZEDSTRING**</dt> </dl>       | Stringa riconosciuta.<br/>                                                                                                                            |
| <span id="GUID_CNP_ROTATEDBOUNDINGBOX"></span><span id="guid_cnp_rotatedboundingbox"></span><dl> <dt>**GUID \_ CNP \_ ROTATEDBOUNDINGBOX**</dt> </dl> | Rettangolo di delimitazione ruotato.<br/>                                                                                                                         |
| <span id="GUID_CNP_SEMANTICTYPE"></span><span id="guid_cnp_semantictype"></span><dl> <dt>**GUID \_ CNP \_ SEMANTICTYPE**</dt> </dl>                   | La proprietà contiene informazioni sui tipi semantici utilizzati nella definizione di un'annotazione, ad esempio se si tratta di un callout, di un commento e così via.<br/> |
| <span id="GUID_CNP_SHAPENAME"></span><span id="guid_cnp_shapename"></span><dl> <dt>**GUID \_ CNP \_ ShapeName**</dt> </dl>                            | Nome della forma di un nodo di disegno input penna.<br/>                                                                                                            |



## <a name="remarks"></a>Commenti

Questi GUID vengono usati per identificare le proprietà che [**IInkAnalyzer**](iinkanalyzer.md) può impostare in un [**IContextNode**](icontextnode.md). Ink Analyzer imposta alcuni dati della proprietà in base al tipo del nodo di contesto (vedere [**IContextNode:: GetType**](icontextnode-gettype.md)).

Per ottenere o impostare proprietà specifiche per i nodi hint di analisi, vedere [**proprietà hint di analisi**](analysis-hint-properties.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Iaguid. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà hint di analisi](analysis-hint-properties.md)
</dt> <dt>

[Tipi di nodo di contesto](context-node-types.md)
</dt> <dt>

[**IContextNode:: ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode:: LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode:: RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode:: SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




