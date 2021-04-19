---
description: La proprietà SourceDir è la directory radice che contiene il file CAB di origine o l'albero dei file di origine del pacchetto di installazione. Questo valore viene usato per la risoluzione della directory.
ms.assetid: 900b26e8-80dd-4e70-8d79-37f09a0c6e86
title: Proprietà SourceDir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a366e4afecdd16722a06ecfbec08552baab8f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332605"
---
# <a name="sourcedir-property"></a>Proprietà SourceDir

La proprietà **SourceDir** è la directory radice che contiene il file CAB di origine o l'albero dei file di origine del pacchetto di installazione. Questo valore viene usato per la risoluzione della directory.

## <a name="default-value"></a>Valore predefinito

Directory che contiene il pacchetto di installazione.

## <a name="remarks"></a>Commenti

L' [azione ResolveSource](resolvesource-action.md) deve essere chiamata prima di usare la proprietà **SourceDir** in qualsiasi espressione o tentare di recuperare il valore di **SourceDir** con [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya). L'azione ResolveSource non deve essere eseguita mentre l'origine non è disponibile, ad esempio quando si disinstalla un'applicazione, perché ciò può causare una richiesta non intenzionale per il supporto di origine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




