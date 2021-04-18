---
description: Consente al filtro di elaborazione delle immagini di scrivere di nuovo le proprietà sul driver (e sul dispositivo).
ms.assetid: b9bb8d81-2945-46ba-a0a2-7009000574aa
title: 'Metodo IWiaImageFilter:: ApplyProperties (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.ApplyProperties
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3c20527ee587b975adea34e7c480349836620015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312397"
---
# <a name="iwiaimagefilterapplyproperties-method"></a>Metodo IWiaImageFilter:: ApplyProperties

Consente al filtro di elaborazione delle immagini di scrivere di nuovo le proprietà sul driver (e sul dispositivo).

## <a name="syntax"></a>Sintassi


```C++
HRESULT ApplyProperties(
  [in] IWiaPropertyStorage *pWiaPropertyStorage
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pWiaPropertyStorage* \[ in\]
</dt> <dd>

Tipo: **[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) \** _

Specifica un puntatore a [_ *IWiaPropertyStorage* *](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) per le proprietà da applicare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Non chiamare questo metodo direttamente dall'applicazione. Viene chiamato da Windows Image Acquisition (WIA) 2,0 dopo che il filtro di elaborazione delle immagini ha elaborato i dati non elaborati.

*pWiaPropertyStorage* è l'interfaccia [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) in cui il filtro di elaborazione delle immagini deve scrivere le proprietà. Un filtro di elaborazione immagini deve usare solo il metodo [IPropertyStorage:: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) per scrivere le proprietà.

Questo metodo consente al filtro di elaborazione delle immagini di scrivere di nuovo le proprietà nel driver (e nel dispositivo). Questa operazione può essere necessaria per i filtri che implementano funzionalità come l'esposizione automatica durante l'analisi dei film.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
