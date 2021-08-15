---
description: Imposta o recupera il percorso di ricerca di Active Directory.
ms.assetid: 43320799-1c01-4e09-bed9-f3576baadcce
title: Impostazioni. ActiveDirectorySearchLocation - proprietà
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
ms.openlocfilehash: 884866fd5ff6a3e3ff483a255bf2b77063ca81e51141108c9f58fd45629cc036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900321"
---
# <a name="settingsactivedirectorysearchlocation-property"></a>Impostazioni. ActiveDirectorySearchLocation - proprietà

\[La **proprietà ActiveDirectorySearchLocation** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti.\]

La **proprietà ActiveDirectorySearchLocation** imposta o recupera il percorso di ricerca di Active Directory.

## <a name="syntax"></a>Sintassi


```VB
Settings.ActiveDirectorySearchLocation As CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
```



## <a name="property-value"></a>Valore proprietà

Valore dell'enumerazione [**CAPICOM \_ ACTIVE DIRECTORY SEARCH \_ \_ \_ LOCATION**](capicom-active-directory-search-location.md) che specifica il percorso di ricerca. Il valore predefinito è CAPICOM \_ SEARCH \_ ANY. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                           | Significato                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="CAPICOM_SEARCH_ANY"></span><span id="capicom_search_any"></span><dl> <dt>**CAPICOM \_ SEARCH \_ ANY**</dt> </dl>                                   | Eseguire la ricerca in tutte le località disponibili.<br/> |
| <span id="CAPICOM_SEARCH_DEFAULT_DOMAIN"></span><span id="capicom_search_default_domain"></span><dl> <dt>**DOMINIO \_ PREDEFINITO \_ DELLA RICERCA CAPICOM \_**</dt> </dl> | Cercare solo il dominio predefinito.<br/> |
| <span id="CAPICOM_SEARCH_GLOBAL_CATALOG"></span><span id="capicom_search_global_catalog"></span><dl> <dt>**CAPICOM \_ SEARCH \_ GLOBAL \_ CATALOG**</dt> </dl> | Eseguire la ricerca solo nel catalogo globale.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Impostazioni**](settings.md)
</dt> </dl>

 

 




