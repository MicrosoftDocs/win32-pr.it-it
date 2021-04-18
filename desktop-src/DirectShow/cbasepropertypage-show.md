---
description: 'Il metodo Show Visualizza o nasconde la finestra di dialogo. Questo metodo implementa il Metodo IPropertyPage:: Show.'
ms.assetid: 03796779-ed41-4b68-852d-6b1849a9dc10
title: Metodo CBasePropertyPage. Show (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Show
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1dadd1c187773df3ca41ac0e1e4daf06fb54761b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330407"
---
# <a name="cbasepropertypageshow-method"></a>CBasePropertyPage. Show (metodo)

Il `Show` Metodo Visualizza o nasconde la finestra di dialogo. Questo metodo implementa il metodo [IPropertyPage:: Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) .

## <a name="syntax"></a>Sintassi

```C++
HRESULT Show(
   UINT nCmdShow
);
```
## <a name="parameters"></a>Parametri

*nCmdShow*

Tipo: **[uint](../winprog/windows-data-types.md)**

Valore che specifica se visualizzare o nascondere la finestra. Per ulteriori informazioni, vedere il metodo [IPropertyPage:: Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) .

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Di seguito sono indicati alcuni valori possibili.

| Codice restituito                                                                                  | Descrizione                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Esito positivo.<br/>            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argomento non valido.<br/>   |
| <dl> <dt>**E \_ imprevisto**</dt> </dl> | Errore imprevisto.<br/> |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione  | <dl> <dt>Cprop. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |

## <a name="see-also"></a>Vedi anche

[Classe CBasePropertyPage](cbasepropertypage.md)
