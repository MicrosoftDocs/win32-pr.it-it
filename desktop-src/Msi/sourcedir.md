---
description: La proprietà SourceDir è la directory radice che contiene il file CAB di origine o l'albero dei file di origine del pacchetto di installazione. Questo valore viene usato per la risoluzione della directory.
ms.assetid: 900b26e8-80dd-4e70-8d79-37f09a0c6e86
title: SourceDir - proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163fde883708f1c842a2cc1483f7558accb79129446554252dc3d18f2a2fe939
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117989989"
---
# <a name="sourcedir-property"></a>SourceDir - proprietà

La **proprietà SourceDir** è la directory radice che contiene il file CAB di origine o l'albero dei file di origine del pacchetto di installazione. Questo valore viene usato per la risoluzione della directory.

## <a name="default-value"></a>Valore predefinito

Directory che contiene il pacchetto di installazione.

## <a name="remarks"></a>Commenti

[L'azione ResolveSource](resolvesource-action.md) deve essere chiamata prima di usare la proprietà **SourceDir** in qualsiasi espressione o di tentare di recuperare il valore di **SourceDir** con [**MsiGetProperty.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) L'azione ResolveSource non deve essere eseguita mentre l'origine non è disponibile, ad esempio quando si disinstalla un'applicazione, perché ciò può causare una richiesta imprevista per il supporto di origine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




