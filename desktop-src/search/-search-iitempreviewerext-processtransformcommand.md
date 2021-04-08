---
description: Consente l'elaborazione di un comando di trasformazione rilevato in un modello di anteprima.
ms.assetid: 0b81b780-8bd1-4667-a0a1-65319f209603
title: IItemPreviewerExt::P metodo rocessTransformCommand
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
ms.openlocfilehash: 384294aac177679ea7445edb880198d250310625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878817"
---
# <a name="iitempreviewerextprocesstransformcommand-method"></a>IItemPreviewerExt::P metodo rocessTransformCommand

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

*dwContext* \[ in\]
</dt> <dd>

Tipo: **DWORD**

Identificatore di contesto per l'operazione. Eseguire l'override dell'impostazione predefinita *dwContext* per impostare l'identificatore di contesto su un valore a scelta.

</dd> <dt>

*pwszName* \[ in\]
</dt> <dd>

Tipo: **LPCOLESTR**

Puntatore al nome del comando di trasformazione come stringa Unicode.

</dd> <dt>

*pwszArg* \[ in\]
</dt> <dd>

Tipo: **LPCOLESTR**

Puntatore all'argomento come stringa Unicode.

</dd> <dt>

*pvarResult* \[ out, retval\]
</dt> <dd>

Tipo: **Variant \** _

Puntatore alla variante di risultato. _pvarResult * non deve essere un puntatore **null** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

L'interfaccia [**IItemPreviewerExt**](-search-iitempreviewerext.md) è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.

Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia [**IItemPreviewerExt**](-search-iitempreviewerext.md) e le API seguenti: le interfacce [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , la struttura [**LINKINFO**](-search-linkinfo.md) e l'enumerazione [**LinkType**](-search-linktype.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/> |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IItemPreviewerExt**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




