---
title: Proprietà IsUpdateNeeded di IResultsViewer (WdsView.h)
description: Restituisce TRUE se la query delle viste è stata modificata ed è necessario aggiornarsi.
ms.assetid: 68ae1f68-0585-4bc5-bea4-eb55f3626093
keywords:
- Proprietà IsUpdateNeeded Funzionalità dell'Windows legacy
- Proprietà IsUpdateNeeded legacy Windows dell'ambiente, interfaccia IResultsViewer
- Interfaccia IResultsViewer legacy Windows funzionalità dell'ambiente , proprietà IsUpdateNeeded
topic_type:
- apiref
api_name:
- IResultsViewer.IsUpdateNeeded
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c013692509ddebe5c0f6530e9abf4b17aa2c356c6eade829bdc2dbad52465f27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753882"
---
# <a name="iresultsviewerisupdateneeded-property"></a>Proprietà IResultsViewer::IsUpdateNeeded

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Restituisce TRUE se la query delle viste è stata modificata ed è necessario aggiornarsi.

## <a name="syntax"></a>Sintassi

## <a name="property-value"></a>Valore proprietà

Quando viene chiamato, restituirà un puntatore al flag che indica se la query è stata modificata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                 |
| Server minimo supportato<br/> | Windows Solo Server 2003 con app desktop SP1 \[\]<br/>                        |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>WdsView.h</dt> </dl> |



 

 





