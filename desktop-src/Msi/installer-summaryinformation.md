---
description: La proprietà SummaryInformation dell'oggetto Installer restituisce un oggetto SummaryInfo che può essere utilizzato per esaminare, aggiornare e aggiungere proprietà al flusso di informazioni di riepilogo di un pacchetto o di una trasformazione.
ms.assetid: 6a1d81b9-d61f-4bff-92c3-35fc436a6a41
title: Proprietà Installer. SummaryInformation
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
ms.openlocfilehash: 1ee593ca2ffebf3ca5574a8e2a6547b9cd81be40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325290"
---
# <a name="installersummaryinformation-property"></a>Proprietà Installer. SummaryInformation

La proprietà **SummaryInformation** dell'oggetto [**Installer**](installer-object.md) restituisce un oggetto [**SummaryInfo**](summaryinfo-object.md) che può essere utilizzato per esaminare, aggiornare e aggiungere proprietà al flusso di informazioni di riepilogo di un pacchetto o di una trasformazione.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.SummaryInformation
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Se viene usato un valore di *maxProperties* maggiore di 0 per aprire un flusso di informazioni di riepilogo esistente, è necessario chiamare il metodo di [**salvataggio permanente**](summaryinfo-persist.md) prima di chiudere l'oggetto. In caso contrario, le informazioni sul flusso esistenti vengono perse.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




