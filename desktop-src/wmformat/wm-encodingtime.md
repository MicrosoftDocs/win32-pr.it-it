---
title: WM/EncodingTime
description: L'attributo WM/EncodingTime contiene un timestamp dell'ora in cui è stato codificato il contenuto.
ms.assetid: 63da9392-264d-40bb-99fd-56db93801941
keywords:
- WM/EncodingTime windows Media Format
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20c76de789bd6ca88a9bbc2f3bb68381b3816524a07cbf97dc1a35b2526179a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431841"
---
# <a name="wmencodingtime"></a>WM/EncodingTime

**L'attributo WM/EncodingTime** contiene un timestamp dell'ora in cui è stato codificato il contenuto.

## <a name="global-constant"></a>Costante globale

g \_ wszWMEncodingTime

## <a name="data-type"></a>Tipo di dati

**FILETIME** (**WMT \_ TYPE \_ QWORD**)

## <a name="remarks"></a>Commenti

Questo attributo usa un valore FILETIME, ovvero un valore a 64 bit che rappresenta il numero di unità di tempo di 100 nanosecondi trascorse dal 1° gennaio 1601. Per altre informazioni su FILETIME, vedere la Windows System Information di Platform SDK.

Non si tratta di un attributo codificato. È necessario impostarlo manualmente se si vuole includerlo nei file.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




