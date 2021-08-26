---
description: AdminProperties deve essere creato nella tabella delle proprietà.
ms.assetid: 91dd58cf-6c8c-4d20-a829-c43301a30d7f
title: AdminProperties - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f59d2452e244bd22110ab918dff61279bf9d27f3c8735f37474aea894d0d02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078131"
---
# <a name="adminproperties-property"></a>AdminProperties - proprietà

AdminProperties **deve** essere creato nella tabella [delle proprietà](property-table.md). Il valore di **AdminProperties** è un elenco di nomi di proprietà separati da punti e virgola. Il programma di installazione salva i valori di queste proprietà elencate al momento di [un'installazione amministrativa](administrative-installation.md)di . Quando gli utenti installano dall'immagine amministrativa, l'installazione usa i valori salvati delle proprietà, anziché i valori nel file .msi.

## <a name="remarks"></a>Commenti

I nomi delle proprietà nell'elenco possono essere lettere maiuscole e minuscole (proprietà private) o tutte maiuscole (proprietà pubbliche).

Questa proprietà non deve mai terminare con un punto e virgola.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




