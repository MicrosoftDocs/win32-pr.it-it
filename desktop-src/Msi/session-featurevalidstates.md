---
description: La proprietà FeatureValidStates dell'oggetto Session restituisce un Integer che rappresenta i flag di bit con ogni bit pertinente che rappresenta uno stato di installazione valido per la funzionalità specificata.
ms.assetid: 8a1f6911-b0a6-4fac-ba77-df4f1b7d15e2
title: Proprietà Session. FeatureValidStates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureValidStates
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b76080bb7854c75cbfbb06697de9fc7d7a1af0c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330775"
---
# <a name="sessionfeaturevalidstates-property"></a>Proprietà Session. FeatureValidStates

La proprietà **FeatureValidStates** dell'oggetto [**Session**](session-object.md) restituisce un Integer che rappresenta i flag di bit con ogni bit pertinente che rappresenta uno stato di installazione valido per la funzionalità specificata.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Session.FeatureValidStates
```



## <a name="property-value"></a>Valore proprietà

Nome di stringa obbligatorio dell'elemento della funzionalità di cui devono essere recuperati gli Stati di installazione validi.

## <a name="remarks"></a>Commenti

Il valore restituito è costituito da flag di bit, come indicato di seguito. Bit 0: se impostato, local è uno stato valido. Bit 1: se impostato, l'origine è uno stato valido.

La proprietà **FeatureValidStates** ha esito positivo solo dopo che il programma di installazione ha chiamato le azioni [CostInitialize](costinitialize-action.md) e [CostFinalize secondo](costfinalize-action.md) .

**FeatureValidStates** determina la validità dello stato eseguendo una query su tutti i componenti collegati alla funzionalità specificata senza considerare lo stato di installazione corrente di un componente.

I possibili stati validi per una funzionalità sono determinati come segue:

-   Se la funzionalità non contiene componenti, sia \_ l'origine InstallState locale che quella InstallState \_ sono stati validi per la funzionalità.
-   Se almeno un componente della funzionalità dispone di un attributo di msidbComponentAttributesLocalOnly o msidbComponentAttributesOptional, INSTALLSTATE \_ local è uno stato valido per la funzionalità.
-   Se almeno un componente della funzionalità dispone di un attributo di msidbComponentAttributesSourceOnly o msidbComponentAttributesOptional, INSTALLSTATE \_ source è uno stato valido per la funzionalità.
-   Se un file di un componente appartenente alla funzionalità viene patchato o da un'origine compressa, \_ l'origine InstallState non è inclusa come stato valido per la funzionalità.
-   L'annuncio INSTALLSTATE \_ non è uno stato valido se la funzionalità non consente l'annuncio (msidbFeatureAttributesDisallowAdvertise) o se la funzionalità richiede il supporto della piattaforma per gli annunci (msidbFeatureAttributesNoUnsupportedAdvertise) e la piattaforma non la supporta.
-   INSTALLSTATE \_ assente è uno stato valido per la funzionalità se gli attributi non includono msidbFeatureAttributesUIDisallowAbsent.
-   Gli stati validi per le funzionalità figlio contrassegnate per seguire la funzionalità padre (msidbFeatureAttributesFollowParent) si basano sull'azione o sullo stato di installazione della funzionalità padre.

Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sugli errori usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




