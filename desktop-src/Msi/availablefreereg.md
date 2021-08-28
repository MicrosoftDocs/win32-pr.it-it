---
description: La proprietà AVAILABLEFREEREG specifica in kilobyte lo spazio disponibile totale disponibile nel Registro di sistema dopo la chiamata all'azione AllocateRegistrySpace. Il valore massimo della proprietà AVAILABLEFREEREG è 2000000 kilobyte. Questa proprietà è impostata solo Windows 2000.
ms.assetid: 95afc397-2f28-4ab9-8d95-d071c2f1f498
title: AVAILABLEFREEREG - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b45508494f9ba87ec8261b38ea18f83d0b3ad9796f7390b70349211cbf244df3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650071"
---
# <a name="availablefreereg-property"></a>AVAILABLEFREEREG - proprietà

La **proprietà AVAILABLEFREEREG** specifica in kilobyte lo spazio disponibile totale disponibile nel Registro di sistema dopo la chiamata all'azione [AllocateRegistrySpace](allocateregistryspace-action.md).

Il valore massimo della **proprietà AVAILABLEFREEREG** è 2000000 kilobyte.

Questa proprietà è impostata solo Windows 2000.

## <a name="remarks"></a>Commenti

La **proprietà AVAILABLEFREEREG** deve essere impostata su un valore sufficientemente grande da garantire spazio sufficiente nel Registro di sistema per tutte le informazioni di registrazione aggiunte dall'installazione. Il valore minimo necessario per garantire spazio sufficiente dipende da dove si trova l'azione [AllocateRegistrySpace](allocateregistryspace-action.md) nella sequenza di azioni perché il programma di installazione aumenta automaticamente lo spazio necessario quando si registrano le informazioni nelle tabelle [Registry](registry-table.md), [Class](class-table.md), [SelfReg](selfreg-table.md), [Extension,](extension-table.md) [MIME](mime-table.md)e [Verb.](verb-table.md) Il programma di installazione non aumenta lo spazio totale del Registro di sistema alla quantità specificata da **AVAILABLEFREEREG** fino a raggiungere AllocateRegistrySpace nella sequenza di azioni.

Se AllocateRegistrySpace è una delle prime azioni nella sequenza di azioni, **AVAILABLEFREEREG** deve essere impostato sullo spazio totale richiesto dalle informazioni di registrazione nella tabella Del [](custom-actions.md) Registro di sistema, nella tabella Class, nella tabella TypeLib, nella tabella SelfReg, nella tabella Extension, nella tabella MIME, nella tabella verbo, nella registrazione delle azioni personalizzate, nella registrazione automatica e in qualsiasi altra informazione del Registro di sistema scritta durante l'installazione. Il valore di **AVAILABLEFREEREG** è la quantità totale di informazioni aggiunte dall'installazione e garantisce spazio sufficiente in tutti i casi. Questo è anche il caso più comune.

Se è possibile creare l'azione AllocateRegistrySpace nella sequenza di azioni dopo tutte le azioni [standard](standard-actions.md) che scrivono dati di registrazione, ad esempio [WriteRegistryValues](writeregistryvalues-action.md) e [RegisterClassInfo,](registerclassinfo-action.md)il valore di **AVAILABLEFREEREG** deve essere impostato solo sullo spazio necessario per registrare azioni personalizzate, registrare librerie dei tipi e qualsiasi altra informazione non ancora registrata tramite le tabelle.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




