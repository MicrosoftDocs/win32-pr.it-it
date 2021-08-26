---
description: La proprietà SummaryInformation dell'oggetto Installer restituisce un oggetto SummaryInfo che può essere usato per esaminare, aggiornare e aggiungere proprietà al flusso di informazioni di riepilogo di un pacchetto o di una trasformazione.
ms.assetid: 6a1d81b9-d61f-4bff-92c3-35fc436a6a41
title: Proprietà Installer.SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f671a5424e1008787443a13f2b72e75cb931da2f0783681c360a1b03ad640aff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043621"
---
# <a name="installersummaryinformation-property"></a>Proprietà Installer.SummaryInformation

La **proprietà SummaryInformation** dell'oggetto [**Installer**](installer-object.md) restituisce un [**oggetto SummaryInfo**](summaryinfo-object.md) che può essere usato per esaminare, aggiornare e aggiungere proprietà al flusso di informazioni di riepilogo di un pacchetto o di una trasformazione.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.SummaryInformation
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Se viene usato un valore *maxProperties* maggiore di 0 per aprire un flusso di informazioni di riepilogo esistente, è necessario chiamare il metodo [**Persist**](summaryinfo-persist.md) prima di chiudere l'oggetto. Se non si riesce a eseguire questa operazione, le informazioni sul flusso esistenti vengono persi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller è definito come \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




