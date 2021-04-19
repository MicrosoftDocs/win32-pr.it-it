---
description: Il metodo ReadXMLFile carica un file di progetto XML.
ms.assetid: 8269da74-fb33-42cf-ae8c-fe3d7db27aea
title: 'Metodo IXml2Dex:: ReadXMLFile (qedit. h)'
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
ms.openlocfilehash: 5b0fb5104e56afbcc4dd25e28981f0c382d7888e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332637"
---
# <a name="ixml2dexreadxmlfile-method"></a>Metodo IXml2Dex:: ReadXMLFile

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `ReadXMLFile` metodo carica un file di progetto XML. Questo metodo consente di creare istanze di tutti gli oggetti espressi nel file XML e di inserirli nella sequenza temporale, nonché di applicare gli attributi specificati per la sequenza temporale, ad esempio la frequenza dei fotogrammi o l'effetto predefinito.

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

Puntatore all'interfaccia **IUnknown** di un oggetto della sequenza temporale.

</dd> <dt>

*XMLName* 
</dt> <dd>

Stringa che specifica il nome del file da caricare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore HRESULT. Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                                  | Descrizione                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                         | Operazione riuscita<br/>             |
| <dl> <dt>**\_formato file VFW E \_ non valido \_ \_**</dt> </dl> | Formato di file non valido<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo non cancella gli oggetti esistenti dalla sequenza temporale prima di inserire i nuovi oggetti definiti nel file XML. Se è necessario aggiornare una sequenza temporale esistente, chiamare prima [**IAMTimeline:: ClearAllGroups**](iamtimeline-clearallgroups.md) .

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Internet Explorer 4,0 o versione successiva<br/>                                               |
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IXml2Dex**](ixml2dex.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




