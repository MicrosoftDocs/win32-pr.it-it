---
description: Ottiene una parte del corpo correlata per l'incorporamento nel flusso MHTML di output.
ms.assetid: 7810568b-5fb7-4814-aa9f-d7ae805c97e1
title: 'Metodo IItemPreviewerExt:: GetRelatedPart'
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
ms.openlocfilehash: 281d91b1679b2a944996bb1c85060d16c4e0b966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306166"
---
# <a name="iitempreviewerextgetrelatedpart-method"></a>Metodo IItemPreviewerExt:: GetRelatedPart

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

*dwContext* \[ in\]
</dt> <dd>

Tipo: **DWORD**

Identificatore di contesto per l'operazione. Eseguire l'override dell'impostazione predefinita **dwContext** per impostare l'identificatore di contesto su un valore a scelta.

</dd> <dt>

*pwszProp* \[ in\]
</dt> <dd>

Tipo: **LPCOLESTR**

Puntatore alla proprietà del contenuto collegato come stringa Unicode.

</dd> <dt>

*dwIndex* \[ in\]
</dt> <dd>

Tipo: **DWORD**

Valore long integer senza segno che contiene l'indice in base zero della parte corpo correlata.

</dd> <dt>

*pInfo* \[ out, retval\]
</dt> <dd>

Tipo: **[**LINKINFO**](-search-linkinfo.md) \** _

Riceve un puntatore alla struttura [_ *LINKINFO* *](-search-linkinfo.md) in cui il metodo restituisce informazioni sulla transazione. *pInfo* non deve essere un puntatore **null** .

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

 

 




