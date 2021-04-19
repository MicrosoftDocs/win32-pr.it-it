---
description: L'impostazione di questa proprietà equivale a impostare i criteri del criterio TransformsAtSource, ad eccezione del fatto che l'ambito è diverso.
ms.assetid: b78c3757-d969-4684-84b9-b2acfd9f5c82
title: Proprietà TRANSFORMSATSOURCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b0acf2e64976d66f04fbd16ec67a5bb38b7fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333022"
---
# <a name="transformsatsource-property"></a>Proprietà TRANSFORMSATSOURCE

L'impostazione di questa proprietà equivale a impostare i criteri del [criterio TransformsAtSource](transformsatsource-policy.md) , ad eccezione del fatto che l'ambito è diverso. L'impostazione del criterio TransformsAtSource si applica a tutti i pacchetti installati da un determinato utente. L'impostazione della proprietà **TRANSFORMSATSOURCE** si applica al pacchetto indipendentemente dagli utenti.

## <a name="remarks"></a>Commenti

Windows Installer interpreta la proprietà **TRANSFORMSATSOURCE** come se fosse la proprietà [**TRANSFORMSSECURE**](transformssecure.md) . Se il flag @ viene passato nella proprietà [**TRANSforms**](transforms.md) , Windows Installer considera le trasformazioni nell'elenco come [trasformazioni sicure all'origine](secure-at-source-transforms.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




