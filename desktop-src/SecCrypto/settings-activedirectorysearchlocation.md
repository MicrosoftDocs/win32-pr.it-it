---
description: Imposta o Recupera il percorso di ricerca Active Directory.
ms.assetid: 43320799-1c01-4e09-bed9-f3576baadcce
title: Proprietà Settings. ActiveDirectorySearchLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.ActiveDirectorySearchLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d218b3d589b76980d468395a39452613aa57ada5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329465"
---
# <a name="settingsactivedirectorysearchlocation-property"></a>Proprietà Settings. ActiveDirectorySearchLocation

\[La proprietà **ActiveDirectorySearchLocation** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.\]

La proprietà **ActiveDirectorySearchLocation** imposta o Recupera il percorso di ricerca Active Directory.

## <a name="syntax"></a>Sintassi


```VB
Settings.ActiveDirectorySearchLocation As CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
```



## <a name="property-value"></a>Valore proprietà

Valore dell'enumerazione del [**\_ percorso di ricerca di \_ Active \_ directory \_ di CAPICOM**](capicom-active-directory-search-location.md) che specifica il percorso di ricerca. Il valore predefinito è CAPICOM \_ ricerca \_ any. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                           | Significato                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="CAPICOM_SEARCH_ANY"></span><span id="capicom_search_any"></span><dl> <dt>**\_ricerca CAPICOM \_**</dt> </dl>                                   | Cerca tutti i percorsi disponibili.<br/> |
| <span id="CAPICOM_SEARCH_DEFAULT_DOMAIN"></span><span id="capicom_search_default_domain"></span><dl> <dt>**\_dominio predefinito di ricerca di CAPICOM \_ \_**</dt> </dl> | Eseguire la ricerca solo nel dominio predefinito.<br/> |
| <span id="CAPICOM_SEARCH_GLOBAL_CATALOG"></span><span id="capicom_search_global_catalog"></span><dl> <dt>**\_catalogo globale di ricerca \_ CAPICOM \_**</dt> </dl> | Eseguire la ricerca solo nel catalogo globale.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Impostazioni**](settings.md)
</dt> </dl>

 

 




