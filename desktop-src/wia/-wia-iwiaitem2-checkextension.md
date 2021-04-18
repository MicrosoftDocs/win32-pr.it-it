---
description: "Verifica se un'estensione specificata è disponibile nel computer e può essere usata dal metodo IWiaItem2:: GetExtension."
ms.assetid: 672f6418-4ce3-4570-a412-fe639c9f5eb8
title: 'Metodo IWiaItem2:: CheckExtension (WIA. h)'
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
ms.openlocfilehash: 65b0b5b3ace1634a20dfa63382d82099fef0686e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308222"
---
# <a name="iwiaitem2checkextension-method"></a>Metodo IWiaItem2:: CheckExtension

Verifica se un'estensione specificata è disponibile nel computer e può essere usata dal metodo [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md) .

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

*è* \[ in\]
</dt> <dd>

Tipo: **Long**

Attualmente non usato. Deve essere impostato su zero.

</dd> <dt>

*bstrName* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Specifica il nome dell'estensione.

</dd> <dt>

*riidExtensionInterface* \[ in\]
</dt> <dd>

Tipo: **REFIID**

Attualmente non usato.

</dd> <dt>

*pbExtensionExists* \[ out\]
</dt> <dd>

Tipo: **bool \** _

Riceve un puntatore a _ * BOOL * *.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE**


</dt> <dd>

L'estensione specificata non è disponibile.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE**


</dt> <dd>

L'estensione specificata è disponibile.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Utilizzando questo metodo, le applicazioni possono verificare se un'estensione è disponibile prima di chiamare il metodo [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md) . Inoltre, l'applicazione può verificare quali estensioni sono disponibili senza co-creazione di ognuna di esse, quindi decidere quale usare.

## <a name="examples"></a>Esempio

CheckImgFilter controlla se il driver ha un filtro di elaborazione delle immagini. Prima di chiamare il componente di anteprima, un'applicazione deve verificare che il driver disponga di un filtro di elaborazione delle immagini.


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




