---
description: La proprietà FeatureRequestState è una proprietà di lettura/scrittura dell'oggetto Session.
ms.assetid: ba19603b-ac81-4a8b-81ca-ad5f28974599
title: Session.FeatureRequestState - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c1198f96dde27ec4056ad099f1bb4a3eed591fdd3d390c843cec42af82d4140e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629221"
---
# <a name="sessionfeaturerequeststate-property"></a>Session.FeatureRequestState - proprietà

La **proprietà FeatureRequestState** è una proprietà di lettura/scrittura dell'oggetto Session. [](session-object.md) Può essere usato per ottenere lo stato di azione corrente di una funzionalità o per richiedere una modifica nell'azione di una funzionalità e delle relative sottofeature. La funzionalità deve essere denominata nella [tabella Funzionalità.](feature-table.md) Se viene richiesta una modifica allo stato dell'azione di una funzionalità, è possibile modificare anche lo stato dell'azione di tutti i componenti della funzionalità modificata. Lo stato dell'azione dei componenti condivisi da più di una funzionalità verrà modificato in base al nuovo stato dell'azione della funzionalità (vedere Osservazioni). La **proprietà FeatureRequestState** può essere usata anche per configurare tutte le funzionalità contemporaneamente specificando la parola chiave ALL anziché un nome di funzionalità specifico.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Session.FeatureRequestState
Session.FeatureRequestState = propVal 
```



## <a name="property-value"></a>Valore proprietà

Stringa obbligatoria che specifica il nome della funzionalità da configurare. Per impostare tutte le funzionalità sullo stato desiderato della richiesta, usare la parola riservata senza distinzione tra maiuscole e minuscole: ALL.

## <a name="remarks"></a>Commenti

Il [**metodo SetInstallLevel**](session-setinstalllevel.md) deve essere chiamato prima di **chiamare FeatureRequestState.**

Se viene richiesto lo stato corrente della funzionalità, la **proprietà FeatureRequestState** restituisce uno dei valori seguenti.



| Nome dello stato di selezione         | Significato                                                               |
|------------------------------|-----------------------------------------------------------------------|
| msiInstallStateUnknown = -1  | Non viene eseguita alcuna azione per la funzionalità. Equivale a Null.       |
| msiInstallStateAdvertised =1 | La funzionalità deve essere annunciata.                                          |
| msiInstallStateAbsent = 2    | La funzionalità deve essere rimossa.                                             |
| msiInstallStateLocal = 3     | La funzionalità deve essere installata come run-local.                              |
| msiInstallStateSource = 4    | La funzionalità deve essere installata come run-from-source.                        |
| msiInstallStateDefault = 5   | La funzionalità deve essere reinstallata con lo stato di azione corrente della funzionalità. |



 

Ad esempio, il codice seguente ottiene lo stato corrente di "MyFeature" da un'azione personalizzata VBScript.


```VB
Dim iRequestState
iRequestState = Session.FeatureRequestState("MyFeature")
```



Se lo stato della funzionalità viene configurato, la **proprietà FeatureRequestState** deve essere impostata su uno dei valori seguenti.



| Nome dello stato di selezione          | Significato                                 |
|-------------------------------|-----------------------------------------|
| msiInstallStateAdvertised = 1 | Annunciare la funzionalità.                  |
| msiInstallStateAbsent = 2     | Rimuovere la funzionalità.                     |
| msiInstallStateLocal = 3      | Installare la funzionalità come run-local.       |
| msiInstallStateSource = 4     | Installare la funzionalità come run-from-source. |



 

Ad esempio, le richieste seguenti da un'azione personalizzata VBScript che "MyFeature" sia installato per l'esecuzione in locale nel computer.


```VB
Session.FeatureRequestState("MyFeature")=3
```



Quando **viene chiamato FeatureRequestState,** il programma di installazione tenta di impostare lo stato dell'azione di ogni componente associato alla funzionalità specificata sullo stato specificato, nel modo migliore possibile. Esistono tuttavia situazioni comuni in cui la richiesta non può essere rispettata completamente. Ad esempio, se una funzionalità è associata a due componenti, il componente A e il componente B, tramite la tabella [FeatureComponents](featurecomponents-table.md) e il componente A ha l'attributo **msidbComponentAttributesLocalOnly** e il componente B ha l'attributo **msidbComponentAttributesSourceOnly.** In questo caso, se **FeatureRequestState** viene chiamato con uno stato richiesto msiInstallStateLocal o msiInstallStateSource, la richiesta non può essere rispettata per entrambi i componenti. In questo caso, entrambi i componenti possono essere attivati con il componente A impostato su msiInstallStateLocal e il componente B impostato su msiInstallStateSource.

Se più funzionalità sono collegate a un singolo componente, lo stato dell'azione finale del componente viene determinato come segue: Se almeno una funzionalità chiama per l'installazione locale del componente, viene installato msiInstallStateLocal. Se almeno una funzionalità chiama per l'esecuzione del componente dal supporto di origine, viene installato msiInstallStateSource. Se almeno una funzionalità chiama per la rimozione del componente, lo stato dell'azione è msiInstallStateAbsent. Per altre informazioni sulla modalità di selezione delle funzionalità per l'installazione, vedere la [tabella Funzionalità.](feature-table.md)

Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il [**metodo LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession è definito \_ come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Sessione**](session-object.md)
</dt> <dt>

[Funzionalità](feature-table.md)
</dt> </dl>

 

 




