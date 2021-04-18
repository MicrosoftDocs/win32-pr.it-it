---
description: La proprietà ComponentCosts dell'oggetto Session restituisce un oggetto recordset che enumera lo spazio su disco per ogni unità richiesta per l'installazione di un componente.
ms.assetid: 9b1355f1-cc99-49d9-8187-07fba4804d1f
title: Proprietà Session. ComponentCosts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCosts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a6ef4e3bfd441f5de61c0f3d69aea93d6cfd2ed8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327799"
---
# <a name="sessioncomponentcosts-property"></a>Proprietà Session. ComponentCosts

La proprietà ComponentCosts dell'oggetto [**Session**](session-object.md) [**restituisce un oggetto**](recordlist-object.md) recordset che enumera lo spazio su disco per ogni unità richiesta per l'installazione di un componente. Queste informazioni vengono utilizzate dall'interfaccia utente per visualizzare lo spazio su disco necessario per tutte le unità. I costi di spazio su disco restituiti sono in multipli di 512 byte.

La proprietà ComponentCosts deve essere utilizzata solo dopo che il programma di installazione ha completato il [costo del file](file-costing.md) e dopo l' [azione CostFinalize secondo](costfinalize-action.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Session.ComponentCosts
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Per ottenere il costo totale, aggiungere i costi per tutti i componenti più il costo del motore di installazione (componente = "").

ComponentCosts restituisce un [**oggetto di registrazione**](recordlist-object.md). Ogni record nell'oggetto di registrazione restituito presenta i campi seguenti:



| Campo | Descrizione                                          |
|-------|------------------------------------------------------|
| 1     | Nome volume/unità                                    |
| 2     | Costo dello spazio su disco finale in multipli di 512 byte.     |
| 3     | Costo di spazio su disco temporaneo in multipli di 512 byte. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




