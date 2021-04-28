---
description: "Metodo IMpeg2PsiParser::GetPatVersionNumber: l'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non è un'API DirectShow supportata."
ms.assetid: 2f5ad9bf-3d70-491a-ab45-15cd922a02d4
title: Metodo IMpeg2PsiParser::GetPatVersionNumber
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPatVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 978da4c7076bcf8ffe91bc2b9a4b2077d9d3d48a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089149"
---
# <a name="impeg2psiparsergetpatversionnumber-method"></a>Metodo IMpeg2PsiParser::GetPatVersionNumber

L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non è un'API DirectShow supportata.

Il `GetPatVersionNumber` metodo recupera il campo del numero di versione da \_ PAT. Un flusso di trasporto contiene al massimo un pat. Il numero di versione viene incrementato ogni volta che le informazioni nella tabella vengono cambiate.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPatVersionNumber(
  [out] BYTE *pPatVersion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPatVersion* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve il campo del \_ numero di versione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati, i valori illustrati nella tabella seguente.



| Codice restituito                                                                          | Descrizione         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Operazione completata.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[Esempio di filtro del parser PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




