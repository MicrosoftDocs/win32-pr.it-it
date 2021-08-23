---
description: La proprietà FeatureValidStates dell'oggetto Session restituisce un intero che rappresenta i flag di bit con ogni bit pertinente che rappresenta uno stato di installazione valido per la funzionalità specificata.
ms.assetid: 8a1f6911-b0a6-4fac-ba77-df4f1b7d15e2
title: Session.FeatureValidStates - proprietà
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
ms.openlocfilehash: 2c6b7e2683ea9c3e82684f77057319fb359429036cd43192fa9793ff7490386e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629211"
---
# <a name="sessionfeaturevalidstates-property"></a>Session.FeatureValidStates - proprietà

La **proprietà FeatureValidStates** dell'oggetto [**Session**](session-object.md) restituisce un intero che rappresenta i flag di bit con ogni bit pertinente che rappresenta uno stato di installazione valido per la funzionalità specificata.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Session.FeatureValidStates
```



## <a name="property-value"></a>Valore proprietà

Nome stringa obbligatorio dell'elemento di funzionalità i cui stati di installazione validi devono essere recuperati.

## <a name="remarks"></a>Commenti

Il valore restituito è costituito da flag di bit come indicato di seguito. Bit 0: se impostato, Local è uno stato valido. Bit 1: se impostato, Source è uno stato valido.

La **proprietà FeatureValidStates** ha esito positivo solo dopo che il programma di installazione ha chiamato le azioni [CostInitialize](costinitialize-action.md) [e CostFinalize.](costfinalize-action.md)

**FeatureValidStates determina** la validità dello stato tramite una query su tutti i componenti collegati alla funzionalità specificata senza prendere in considerazione lo stato corrente installato di alcun componente.

I possibili stati validi per una funzionalità sono determinati come segue:

-   Se la funzionalità non contiene componenti, installSTATE LOCAL e \_ INSTALLSTATE \_ SOURCE sono stati validi per la funzionalità.
-   Se almeno un componente della funzionalità ha un attributo msidbComponentAttributesLocalOnly o msidbComponentAttributesOptional, INSTALLSTATE LOCAL è uno stato \_ valido per la funzionalità.
-   Se almeno un componente della funzionalità ha un attributo msidbComponentAttributesSourceOnly o msidbComponentAttributesOptional, INSTALLSTATE SOURCE è uno stato valido \_ per la funzionalità.
-   Se un file di un componente appartenente alla funzionalità è stato patchato o da un'origine compressa, INSTALLSTATE SOURCE non viene incluso come stato valido \_ per la funzionalità.
-   INSTALLSTATE ADVERTISE non è uno stato valido se la funzionalità non consente l'annuncio (msidbFeatureAttributesDisallowAdvertise) o se la funzionalità richiede il supporto della piattaforma per l'annuncio \_ (msidbFeatureAttributesNoUnsupportedAdvertise) e la piattaforma non lo supporta.
-   INSTALLSTATE ABSENT è uno stato valido per la \_ funzionalità se i relativi attributi non includono msidbFeatureAttributesUIDisallowAbsent.
-   Gli stati validi per le funzionalità figlio contrassegnate per seguire la funzionalità padre (msidbFeatureAttributesFollowParent) si basano sull'azione della funzionalità padre o sullo stato installato.

Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il [**metodo LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




