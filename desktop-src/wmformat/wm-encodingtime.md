---
title: WM/EncodingTime
description: L'attributo WM/EncodingTime contiene un timestamp del momento in cui è stato codificato il contenuto.
ms.assetid: 63da9392-264d-40bb-99fd-56db93801941
keywords:
- Formato di Windows Media WM/EncodingTime
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d27119a9b54e3de22fe620f556c672bd4fe1a17
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045929"
---
# <a name="wmencodingtime"></a>WM/EncodingTime

L'attributo **WM/EncodingTime** contiene un timestamp del momento in cui è stato codificato il contenuto.

## <a name="global-constant"></a>Costante globale

g \_ wszWMEncodingTime

## <a name="data-type"></a>Tipo di dati

**FILETIME** (**\_ tipo WMT \_ QWORD**)

## <a name="remarks"></a>Commenti

Questo attributo utilizza un valore FILETIME, ovvero un valore a 64 bit che rappresenta il numero di unità di tempo 100-nanosecondi trascorsi dal 1 ° gennaio 1601. Per ulteriori informazioni su FILETIME, vedere la sezione informazioni di sistema Windows di Platform SDK.

Non si tratta di un attributo codificato. È necessario impostarla manualmente se si vuole includerla nei file.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




