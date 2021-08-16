---
description: Suggerisce i criteri di sicurezza da applicare al browser.
ms.assetid: 73541611-2024-4c33-ab03-e3204244c46c
title: Metodo IItemPreviewerExt::SuggestBrowserPolicy
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
ms.openlocfilehash: 84446b49ab723f161de8f148e95916202efe06176191e820ab8bafc88ed9158a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969760"
---
# <a name="iitempreviewerextsuggestbrowserpolicy-method"></a>Metodo IItemPreviewerExt::SuggestBrowserPolicy

Suggerisce i criteri di sicurezza da applicare al browser.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SuggestBrowserPolicy(
  [in]          DWORD dwContext,
  [out, retval] DWORD *pdwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Oggetto dwContext* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD**

Identificatore di contesto per l'operazione. Eseguire *l'override dell'impostazione predefinita di dwContext* per impostare l'identificatore di contesto su un valore a scelta.

</dd> <dt>

*pdwFlags* \[ out, retval\]
</dt> <dd>

Tipo: **DWORD \***

Puntatore a un valore DWORD contenente i flag di controllo di verifica. Il flag **BROWSERPOLICY \_ UNTRUSTED \_ CONTENT** disabilita qualsiasi possibilità che l'anteprima sia in grado di eseguire script o ActiveX. Il parametro *pdwFlags* non deve essere un **puntatore NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

[**L'interfaccia IItemPreviewerExt**](-search-iitempreviewerext.md) è supportata solo in Windows XP e Windows Server 2003 e non deve più essere usata.

Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti nei computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia [**IItemPreviewerExt**](-search-iitempreviewerext.md) e le API seguenti: le interfacce [**ISearchProtocolUI,**](-search-isearchprotocolui.md) [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem,**](-search-isearchitem.md) la struttura [**LINKINFO**](-search-linkinfo.md) e l'enumerazione [**LINKTYPE.**](-search-linktype.md)

È consigliabile usare il flag **BROWSERPOLICY \_ UNTRUSTED \_ CONTENT** per disabilitare qualsiasi possibilità che l'anteprima sia in grado di eseguire script o ActiveX. Il **metodo IItemPreviewerExt::SuggestBrowserPolicy** può restituire informazioni sull'attendibilità o meno dell'elemento visualizzato in anteprima. In questo modo il controllo trident del visualizzatore di anteprima può eseguire lo script e anche ActiveX controlli. Poiché il visualizzatore anteprima usa spesso file temporanei per generare l'anteprima, questa operazione può comportare l'esecuzione imprevista di script e codice nell'area Computer locale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3.0<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IItemPreviewerExt**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




