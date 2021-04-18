---
description: La proprietà FeatureRequestState è una proprietà di lettura/scrittura dell'oggetto Session.
ms.assetid: ba19603b-ac81-4a8b-81ca-ad5f28974599
title: Proprietà Session. FeatureRequestState
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
ms.openlocfilehash: 1531157ab094d817d34650f8eae2ac6dc23c681c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327798"
---
# <a name="sessionfeaturerequeststate-property"></a>Proprietà Session. FeatureRequestState

La proprietà **FeatureRequestState** è una proprietà di lettura/scrittura dell'oggetto [**Session**](session-object.md) . Può essere utilizzato per ottenere lo stato dell'azione corrente di una funzionalità o per richiedere una modifica nell'azione di una funzionalità e delle relative funzionalità. La funzionalità deve essere denominata nella tabella [feature](feature-table.md) . Se viene richiesta una modifica allo stato dell'azione di una funzionalità, è possibile che venga modificato anche lo stato dell'azione di tutti i componenti della funzionalità modificata. Lo stato dell'azione dei componenti condivisi da più di una funzionalità verrà modificato in base al nuovo stato dell'azione della funzionalità (vedere la sezione Osservazioni). La proprietà **FeatureRequestState** può essere utilizzata anche per configurare tutte le funzionalità contemporaneamente specificando la parola chiave all anziché un nome di funzionalità specifico.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Session.FeatureRequestState
Session.FeatureRequestState = propVal 
```



## <a name="property-value"></a>Valore proprietà

Stringa obbligatoria che specifica il nome della funzionalità da configurare. Per impostare tutte le funzionalità su uno stato di richiesta desiderato, utilizzare la parola riservata senza distinzione tra maiuscole e minuscole: ALL.

## <a name="remarks"></a>Commenti

Il metodo [**SetInstallLevel**](session-setinstalllevel.md) deve essere chiamato prima di chiamare **FeatureRequestState**.

Se viene richiesto lo stato corrente della funzionalità, la proprietà **FeatureRequestState** restituisce uno dei valori seguenti.



| Nome stato selezione         | Significato                                                               |
|------------------------------|-----------------------------------------------------------------------|
| msiInstallStateUnknown =-1  | Non viene eseguita alcuna azione per la funzionalità. Equivale a null.       |
| msiInstallStateAdvertised = 1 | La funzionalità deve essere annunciata.                                          |
| msiInstallStateAbsent = 2    | La funzionalità deve essere rimossa.                                             |
| msiInstallStateLocal = 3     | La funzionalità deve essere installata come run-local.                              |
| msiInstallStateSource = 4    | La funzionalità deve essere installata come esecuzione dall'origine.                        |
| msiInstallStateDefault = 5   | La funzionalità deve essere reinstallata con lo stato dell'azione corrente della funzionalità. |



 

Il codice seguente, ad esempio, ottiene lo stato corrente di "funzionalità" da un'azione personalizzata VBScript.


```VB
Dim iRequestState
iRequestState = Session.FeatureRequestState("MyFeature")
```



Se è in corso la configurazione dello stato della funzionalità, la proprietà **FeatureRequestState** deve essere impostata su uno dei valori seguenti.



| Nome stato selezione          | Significato                                 |
|-------------------------------|-----------------------------------------|
| msiInstallStateAdvertised = 1 | Annunciare la funzionalità.                  |
| msiInstallStateAbsent = 2     | Rimuovere la funzionalità.                     |
| msiInstallStateLocal = 3      | Installare la funzionalità come run-local.       |
| msiInstallStateSource = 4     | Installare la funzionalità come Run-from-source. |



 

Ad esempio, le seguenti richieste da un'azione personalizzata VBScript che "funzionalità" deve essere installata per l'esecuzione locale nel computer.


```VB
Session.FeatureRequestState("MyFeature")=3
```



Quando viene chiamato **FeatureRequestState** , il programma di installazione tenta di impostare sullo stato specificato lo stato dell'azione di ogni componente associato alla funzionalità specificata, nel modo più appropriato possibile. Tuttavia, esistono situazioni comuni in cui la richiesta non può essere pienamente rispettata. Se, ad esempio, una funzionalità è associata a due componenti, il componente A e il componente B, tramite la tabella [FeatureComponents](featurecomponents-table.md) e il componente a, l'attributo **msidbComponentAttributesLocalOnly** e il componente b hanno l'attributo **msidbComponentAttributesSourceOnly** . In questo caso, se **FeatureRequestState** viene chiamato con uno stato richiesto di MsiInstallStateLocal o msiInstallStateSource, la richiesta non può essere rispettata per entrambi i componenti. In questo caso, entrambi i componenti possono essere attivati con componente A impostato su msiInstallStateLocal e il componente B è impostato su msiInstallStateSource.

Se più di una funzionalità è collegata a un singolo componente, lo stato dell'azione finale di tale componente viene determinato nel modo seguente: se almeno una funzionalità richiede che il componente venga installato localmente, viene installato msiInstallStateLocal. Se almeno una funzionalità richiede che il componente venga eseguito dal supporto di origine, viene installato msiInstallStateSource. Se almeno una funzionalità chiama per la rimozione del componente, lo stato dell'azione è msiInstallStateAbsent. Per ulteriori informazioni sulla modalità di selezione delle funzionalità per l'installazione, vedere la tabella delle [funzionalità](feature-table.md) .

Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sugli errori usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Sessione**](session-object.md)
</dt> <dt>

[Funzionalità](feature-table.md)
</dt> </dl>

 

 




