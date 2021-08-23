---
description: Il metodo ReadXMLFile carica un file di progetto XML.
ms.assetid: 8269da74-fb33-42cf-ae8c-fe3d7db27aea
title: Metodo IXml2Dex::ReadXMLFile (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.ReadXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 37df0c93a17dadc2f6d6fbf94a662b89bf9630a0b0861f5bf5a0c676f7d369fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952440"
---
# <a name="ixml2dexreadxmlfile-method"></a>Metodo IXml2Dex::ReadXMLFile

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `ReadXMLFile` metodo carica un file di progetto XML. Questo metodo crea istanze di tutti gli oggetti espressi nel file XML e le inserisce nella sequenza temporale, nonché applica gli attributi specificati per la sequenza temporale, ad esempio la frequenza dei fotogrammi o l'effetto predefinito.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReadXMLFile(
   IUnknown *pTimeline,
   BSTR     XMLName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTimeline* 
</dt> <dd>

Puntatore all'interfaccia **IUnknown** di un oggetto sequenza temporale.

</dd> <dt>

*XMLName* 
</dt> <dd>

Stringa che specifica il nome del file da caricare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore HRESULT. Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                                  | Descrizione                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Operazione riuscita<br/>             |
| <dl> <dt>**FORMATO DI FILE VFW \_ E \_ NON \_ \_ VALIDO**</dt> </dl> | Formato di file non valido<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo non cancella gli oggetti esistenti dalla sequenza temporale prima di inserire i nuovi oggetti definiti nel file XML. Se è necessario aggiornare una sequenza temporale esistente, chiamare [**prima IAMTimeline::ClearAllGroups.**](iamtimeline-clearallgroups.md)

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Internet Explorer 4.0 o versione successiva<br/>                                               |
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IXml2Dex**](ixml2dex.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




