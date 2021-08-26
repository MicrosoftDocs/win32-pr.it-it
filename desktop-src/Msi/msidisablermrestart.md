---
description: La proprietà MSIDISABLERMRESTART determina in che modo le applicazioni o i servizi che attualmente usano i file interessati da un aggiornamento devono essere arrestati e riavviati per abilitare l'installazione dell'aggiornamento.
ms.assetid: 45c804bf-6d15-416a-b106-d8bb3f4c547d
title: MSIDISABLERMRESTART - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d46bdaee34b154ccaacddc36dcb08113fce9e3f749090eb80176080a60235e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042791"
---
# <a name="msidisablermrestart-property"></a>MSIDISABLERMRESTART - proprietà

La **proprietà MSIDISABLERMRESTART** determina in che modo le applicazioni o i servizi che attualmente usano i file interessati da un aggiornamento devono essere arrestati e riavviati per abilitare l'installazione dell'aggiornamento.

## <a name="value"></a>Valore



| Valore                                                                        | Significato                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Tutti i servizi di sistema arrestati per installare l'aggiornamento vengono riavviati. Tutte le applicazioni che si sono registrate con [Gestione riavvio](../rstmgr/restart-manager-portal.md) vengono riavviate.<br/> |
| <dl> <dt>1</dt> </dl> | I processi arrestati con [](../rstmgr/restart-manager-portal.md) Gestione riavvio durante l'installazione dell'aggiornamento non verranno riavviati dopo l'applicazione dell'aggiornamento.<br/>                           |



 

## <a name="remarks"></a>Commenti

La **proprietà MSIDISABLERMRESTART** viene ignorata se [Gestione riavvio](../rstmgr/restart-manager-portal.md) non è disponibile o è disabilitato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Per informazioni Windows sul Service Pack minimo richiesto [da una](windows-installer-portal.md) versione Run-Time programma di installazione di Windows, vedere i requisiti di installazione di Windows.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 3.1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
