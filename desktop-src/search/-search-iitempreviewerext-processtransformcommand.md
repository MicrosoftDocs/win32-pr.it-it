---
description: Consente l'elaborazione di un comando di trasformazione rilevato in un modello di anteprima.
ms.assetid: 0b81b780-8bd1-4667-a0a1-65319f209603
title: Metodo IItemPreviewerExt::P rocessTransformCommand
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.ProcessTransformCommand
api_type:
- COM
api_location: ''
ms.openlocfilehash: f93d4be0bf9491c4fd2f6074c00692d6f634704ec820a34baeb4f1d52343c36a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969777"
---
# <a name="iitempreviewerextprocesstransformcommand-method"></a>Metodo IItemPreviewerExt::P rocessTransformCommand

Consente l'elaborazione di un comando di trasformazione rilevato in un modello di anteprima.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ProcessTransformCommand(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszName,
  [in]          LPCOLESTR pwszArg,
  [out, retval] VARIANT   *pvarResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwContext* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD**

Identificatore di contesto per l'operazione. Eseguire *l'override dell'impostazione predefinita dwContext* per impostare l'identificatore di contesto su un valore di propria scelta.

</dd> <dt>

*pwszName* \[ Pollici\]
</dt> <dd>

Tipo: **LPCOLESTR**

Puntatore al nome del comando di trasformazione come stringa Unicode.

</dd> <dt>

*pwszArg* \[ Pollici\]
</dt> <dd>

Tipo: **LPCOLESTR**

Puntatore all'argomento come stringa Unicode.

</dd> <dt>

*pvarResult* \[ out, retval\]
</dt> <dd>

Tipo: **\* VARIANT**

Puntatore alla variante del risultato. *pvarResult non* deve essere un **puntatore NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

[**L'interfaccia IItemPreviewerExt**](-search-iitempreviewerext.md) è supportata solo in Windows XP e Windows Server 2003 e non deve più essere usata.

Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti nei computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia [**IItemPreviewerExt**](-search-iitempreviewerext.md) e le API seguenti: le interfacce [**ISearchProtocolUI,**](-search-isearchprotocolui.md) [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem,**](-search-isearchitem.md) la struttura [**LINKINFO**](-search-linkinfo.md) e l'enumerazione [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3.0<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IItemPreviewerExt**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




