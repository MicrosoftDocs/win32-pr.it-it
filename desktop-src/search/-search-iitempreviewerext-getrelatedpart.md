---
description: Ottiene una parte del corpo correlata per l'incorporamento nel flusso MHTML di output.
ms.assetid: 7810568b-5fb7-4814-aa9f-d7ae805c97e1
title: Metodo IItemPreviewerExt::GetRelatedPart
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetRelatedPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9abc4415eef014697376c9df4b89af47037a99df5c9ab5a3c74a3d7825b344c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863974"
---
# <a name="iitempreviewerextgetrelatedpart-method"></a>Metodo IItemPreviewerExt::GetRelatedPart

Ottiene una parte del corpo correlata per l'incorporamento nel flusso MHTML di output.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRelatedPart(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [in]          DWORD     dwIndex,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwContext* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD**

Identificatore di contesto per l'operazione. Eseguire **l'override dell'impostazione predefinita dwContext** per impostare l'identificatore di contesto su un valore di propria scelta.

</dd> <dt>

*pwszProp* \[ Pollici\]
</dt> <dd>

Tipo: **LPCOLESTR**

Puntatore alla proprietà del contenuto collegato come stringa Unicode.

</dd> <dt>

*dwIndex* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD**

Valore long integer senza segno che contiene l'indice in base zero della parte del corpo correlata.

</dd> <dt>

*pInfo* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LINKINFO**](-search-linkinfo.md)\***

Riceve un puntatore alla [**struttura LINKINFO**](-search-linkinfo.md) in cui il metodo restituisce informazioni sulla transazione. *pInfo* non deve essere un **puntatore NULL.**

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

 

 




