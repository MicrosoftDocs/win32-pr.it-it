---
description: La proprietà AVAILABLEFREEREG specifica in kilobyte lo spazio libero totale disponibile nel registro di sistema dopo la chiamata dell'azione AllocateRegistrySpace. Il valore massimo della proprietà AVAILABLEFREEREG è 2 milioni kilobyte. Questa proprietà è impostata solo in Windows 2000.
ms.assetid: 95afc397-2f28-4ab9-8d95-d071c2f1f498
title: Proprietà AVAILABLEFREEREG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 517073748195c47ee27b68adbe70d6c69f3f585b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330635"
---
# <a name="availablefreereg-property"></a>Proprietà AVAILABLEFREEREG

La proprietà **AVAILABLEFREEREG** specifica in kilobyte lo spazio libero totale disponibile nel registro di sistema dopo la chiamata dell' [azione AllocateRegistrySpace](allocateregistryspace-action.md).

Il valore massimo della proprietà **AVAILABLEFREEREG** è 2 milioni kilobyte.

Questa proprietà è impostata solo in Windows 2000.

## <a name="remarks"></a>Commenti

La proprietà **AVAILABLEFREEREG** deve essere impostata su un valore sufficientemente grande da garantire spazio sufficiente nel registro di sistema per tutte le informazioni di registrazione aggiunte dall'installazione. Il valore minimo necessario per garantire uno spazio sufficiente dipende dalla posizione in cui si trova l' [azione AllocateRegistrySpace](allocateregistryspace-action.md) nella sequenza di azione perché il programma di installazione aumenta automaticamente lo spazio necessario per la registrazione delle informazioni nelle tabelle [del registro di sistema](registry-table.md), della [classe](class-table.md), di [selfreg](selfreg-table.md), dell' [estensione](extension-table.md), [MIME](mime-table.md)e dei [verbi](verb-table.md) . Il programma di installazione non aumenta lo spazio totale del registro di sistema per la quantità specificata da **AVAILABLEFREEREG** fino a raggiungere AllocateRegistrySpace nella sequenza di azione.

Se AllocateRegistrySpace è una delle prime azioni nella sequenza di azione, **AVAILABLEFREEREG** deve essere impostato sullo spazio totale richiesto dalle informazioni di registrazione nella tabella del registro di sistema, nella tabella delle classi, nella tabella TypeLib, nella tabella SelfReg, nella tabella di estensione, nella tabella MIME, nella tabella dei verbi, nella registrazione delle [azioni personalizzate](custom-actions.md) , nella registrazione automatica e in qualsiasi altra informazione del registro di sistema scritta durante l'installazione Il valore di **AVAILABLEFREEREG** è la quantità totale di informazioni aggiunte dall'installazione e garantisce spazio sufficiente in tutti i casi. Questo è anche il caso più comune.

Se l'azione AllocateRegistrySpace può essere creata nella sequenza di azione dopo tutte le [azioni standard](standard-actions.md) che scrivono i dati di registrazione, ad esempio [WriteRegistryValori consente](writeregistryvalues-action.md) e [registerClassInfo](registerclassinfo-action.md), il valore di **AVAILABLEFREEREG** deve essere impostato solo sullo spazio necessario per registrare azioni personalizzate, registrare le librerie dei tipi e qualsiasi altra informazione non ancora registrata tramite le tabelle.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




