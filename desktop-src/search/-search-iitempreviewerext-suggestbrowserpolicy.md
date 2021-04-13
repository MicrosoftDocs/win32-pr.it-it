---
description: Suggerisce che i criteri di sicurezza devono essere applicati al browser.
ms.assetid: 73541611-2024-4c33-ab03-e3204244c46c
title: 'Metodo IItemPreviewerExt:: SuggestBrowserPolicy'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.SuggestBrowserPolicy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0a4f248edbfa4a1779016e40d73051d8c1d9acac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484428"
---
# <a name="iitempreviewerextsuggestbrowserpolicy-method"></a>Metodo IItemPreviewerExt:: SuggestBrowserPolicy

Suggerisce che i criteri di sicurezza devono essere applicati al browser.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SuggestBrowserPolicy(
  [in]          DWORD dwContext,
  [out, retval] DWORD *pdwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwContext* \[ in\]
</dt> <dd>

Tipo: **DWORD**

Identificatore di contesto per l'operazione. Eseguire l'override dell'impostazione predefinita *dwContext* per impostare l'identificatore di contesto su un valore a scelta.

</dd> <dt>

*pdwFlags* \[ out, retval\]
</dt> <dd>

Tipo: **DWORD \** _

Puntatore a un valore DWORD contenente i flag di verifica della verifica. Il flag _ *BROWSERPOLICY \_ \_ contenuto non attendibile** Disabilita la possibilità che l'anteprima sia in grado di eseguire script o ActiveX. Il parametro *pdwFlags* non deve essere un puntatore **null** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

L'interfaccia [**IItemPreviewerExt**](-search-iitempreviewerext.md) è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.

Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia [**IItemPreviewerExt**](-search-iitempreviewerext.md) e le API seguenti: le interfacce [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , la struttura [**LINKINFO**](-search-linkinfo.md) e l'enumerazione [**LinkType**](-search-linktype.md) .

L'utilizzo del flag di **\_ \_ contenuto non attendibile BROWSERPOLICY** è fortemente consigliato per disabilitare la possibilità che l'anteprima sia in grado di eseguire script o ActiveX. Il metodo **IItemPreviewerExt:: SuggestBrowserPolicy** può restituire informazioni sull'eventuale attendibilità dell'elemento visualizzato in anteprima. In questo modo il controllo Trident del Visualizzatore anteprime eseguirà lo script e anche i controlli ActiveX. Poiché il Visualizzatore anteprime usa spesso file temporanei per generare l'anteprima, questa operazione può comportare l'esecuzione di script e codice imprevisti nell'area del computer locale.

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

 

 




