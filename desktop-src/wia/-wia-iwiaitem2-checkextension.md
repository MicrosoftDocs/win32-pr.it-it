---
description: Controlla se un'estensione specificata è disponibile nel computer e può essere usata dal metodo IWiaItem2::GetExtension.
ms.assetid: 672f6418-4ce3-4570-a412-fe639c9f5eb8
title: Metodo IWiaItem2::CheckExtension (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CheckExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 50240fbf10155fae555c6cd2e30bf8c86c571b8d52b86e02eab9f5bb11ac17ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965580"
---
# <a name="iwiaitem2checkextension-method"></a>Metodo IWiaItem2::CheckExtension

Controlla se un'estensione specificata è disponibile nel computer e può essere usata dal metodo [**IWiaItem2::GetExtension.**](-wia-iwiaitem2-getextension.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT CheckExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] BOOL   *pbExtensionExists
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lFlags* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Attualmente inutilizzato. Deve essere impostato su zero.

</dd> <dt>

*bstrName* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Specifica il nome dell'estensione.

</dd> <dt>

*riidExtensionInterface* \[ Pollici\]
</dt> <dd>

Tipo: **REFIID**

Attualmente inutilizzato.

</dd> <dt>

*pbExtensionExists* \[ Cambio\]
</dt> <dd>

Tipo: **BOOL \***

Riceve un puntatore a un **oggetto BOOL.**

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False**


</dt> <dd>

L'estensione specificata non è disponibile.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Vero**


</dt> <dd>

L'estensione specificata è disponibile.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Usando questo metodo, le applicazioni possono verificare se un'estensione è disponibile prima di chiamare il [**metodo IWiaItem2::GetExtension.**](-wia-iwiaitem2-getextension.md) Inoltre, l'applicazione può controllare quali estensioni sono disponibili senza creare ognuna di esse e quindi decidere quale usare.

## <a name="examples"></a>Esempio

CheckImgFilter controlla se il driver dispone di un filtro di elaborazione delle immagini. Prima di chiamare il componente di anteprima, un'applicazione deve assicurarsi che il driver abbia un filtro di elaborazione delle immagini.


```C++
HRESULT
CheckImgFilter(
   IN  IWiaItem2 *pWiaItem2,
   OUT BOOL      *pbHasImgFilter)
{
   HRESULT     hr = S_OK;

   if (!pWiaItem2 || !pbHasImgFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
     *pbHasImgFilter = FALSE;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_IMAGEPROC_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->CheckExtension(0,
                                        bstrFilterString,
                                        IID_IWiaSegmentationFilter,
                                        pbHasImgFilter);

         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   return hr;

}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 




