---
description: Creare un nuovo elemento figlio. Aggiunge oggetti IWiaItem2 all'albero IWiaItem2 di un dispositivo.
ms.assetid: 525ee788-3ff4-4def-ae71-4a405c04c6a3
title: Metodo IWiaItem2::CreateChildItem (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CreateChildItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: e7d7215f528c36f6b4f5883be19d5d37c8b76d4d8ad9cacbcaa7a63397337c7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965570"
---
# <a name="iwiaitem2createchilditem-method"></a>Metodo IWiaItem2::CreateChildItem

Creare un nuovo elemento figlio. Aggiunge [**oggetti IWiaItem2**](-wia-iwiaitem2.md) all'albero **IWiaItem2 di un** dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateChildItem(
  [in]  LONG      lItemFlags,
  [in]  LONG      lCreationFlags,
  [in]  BSTR      bstrItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lItemFlags* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Specifica il tipo di elemento WIA 2.0. Vedere [**Flag del tipo di elemento WIA**](-wia-wia-item-type-flags.md).

</dd> <dt>

*lCreationFlags* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Specifica come creare il nuovo elemento.

<dt>

<span id="0"></span>

<span id="0"></span>**0** (0)


</dt> <dd>

Impostare i valori predefiniti per le proprietà dell'elemento figlio.

</dd> <dt>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>**COPIA \_ VALORI \_ DELLE \_ PROPRIETÀ PADRE** (0x40000000)


</dt> <dd>

Copiare i valori di tutte le proprietà di lettura/scrittura dall'elemento padre.

</dd> </dl> </dd> <dt>

*bstrItemName* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Specifica il nome dell'elemento. Questo nome viene aggiunto alla fine del nome dell'elemento padre per generare il nome completo dell'elemento.

</dd> <dt>

*ppIWiaItem2* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Riceve l'indirizzo di un puntatore [**all'interfaccia IWiaItem2**](-wia-iwiaitem2.md) che imposta il **metodo IWiaItem2::CreateChildItem.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Alcuni dispositivi hardware WIA 2.0 consentono alle applicazioni di creare nuovi elementi nell'albero [**IWiaItem2**](-wia-iwiaitem2.md) che rappresenta il dispositivo. Le applicazioni devono testare i dispositivi per verificare se supportano questa funzionalità. Usare l'interfaccia IEnumWIA \_ DEV \_ CAPS per enumerare le funzionalità del dispositivo corrente.

Se il dispositivo consente la creazione di nuovi elementi nell'albero [**IWiaItem2,**](-wia-iwiaitem2.md) richiamando **IWiaItem2::CreateChildItem** viene creato un nuovo oggetto **IWiaItem2** figlio del nodo corrente. Passa un puntatore al nuovo nodo all'applicazione tramite il *parametro ppIWiaItem2.* Le applicazioni devono chiamare [il metodo IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori a interfaccia ricevuti tramite il *parametro ppIWiaItem2.*

Se *lCreationFlags* è COPY \_ PARENT PROPERTY VALUES e \_ \_ *lItemFlags* è zero, la funzione restituisce E \_ INVALIDARG.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
