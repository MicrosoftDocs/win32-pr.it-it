---
description: AdminProperties deve essere creato nella tabella delle proprietà.
ms.assetid: 91dd58cf-6c8c-4d20-a829-c43301a30d7f
title: Proprietà AdminProperties
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 739a0e29526ac7c6d9c094bc492cde1d04cdd0f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333579"
---
# <a name="adminproperties-property"></a>Proprietà AdminProperties

**AdminProperties** deve essere creato nella [tabella delle proprietà](property-table.md). Il valore di **AdminProperties** è un elenco di nomi di proprietà separati da punti e virgola. Il programma di installazione salva i valori di queste proprietà elencate al momento dell' [installazione amministrativa](administrative-installation.md). Quando gli utenti installano dall'immagine amministrativa, l'installazione usa i valori salvati delle proprietà, anziché i valori nel file con estensione msi.

## <a name="remarks"></a>Commenti

I nomi delle proprietà nell'elenco possono essere lettere maiuscole e minuscole (proprietà private) o tutte maiuscole (proprietà pubbliche).

Questa proprietà non deve terminare con un punto e virgola.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




