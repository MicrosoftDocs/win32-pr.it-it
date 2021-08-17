---
title: Interfaccia IRDVTaskPlugin
description: L'interfaccia IRDVTaskPlugin viene implementata da un agente attività di aggiornamento della macchina virtuale per consentire all'agente attività di gestire gli aggiornamenti di sistema per una macchina virtuale.
ms.assetid: e06eb707-be78-4d1f-96d3-21526b167e61
ms.tgt_platform: multiple
keywords:
- Interfaccia IRDVTaskPlugin Servizi Desktop remoto
- Interfaccia IRDVTaskPlugin Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- IRDVTaskPlugin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe76f0b0b92286d5a4b7db5126706fd55bdb6f580c11fda1dcaa55a47be4678c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129170"
---
# <a name="irdvtaskplugin-interface"></a>Interfaccia IRDVTaskPlugin

**L'interfaccia IRDVTaskPlugin** viene implementata  da un agente attività di aggiornamento della macchina virtuale per consentire all'agente attività di gestire gli aggiornamenti di sistema per una macchina virtuale. Questa interfaccia viene utilizzata *dall'agente trigger*, implementato dal sistema host.

## <a name="members"></a>Membri

**L'interfaccia IRDVTaskPlugin** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IRDVTaskPlugin** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia IRDVTaskPlugin** include questi metodi.



| Metodo                                          | Descrizione                                                        |
|:------------------------------------------------|:-------------------------------------------------------------------|
| [**Inizializzare**](irdvtaskplugin-initialize.md) | Chiamato per inizializzare l'agente attività.<br/>                    |
| [**Attività di avvio**](irdvtaskplugin-starttask.md)   | Chiamato per avviare l'attività di aggiornamento nella macchina virtuale.<br/> |
| [**Terminare**](irdvtaskplugin-terminate.md)   | Chiamato quando l'agente attività è in fase di arresto.<br/>          |



 

### <a name="properties"></a>Proprietà

Queste **proprietà sono disponibili nell'interfaccia IRDVTaskPlugin.**



| Proprietà                                                   | Tipo di accesso          | Descrizione                                             |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------|
| [**PluginName**](irdvtaskplugin-pluginname.md)<br/> | Sola lettura<br/> | Contiene il nome visualizzato dell'agente attività.<br/> |



 

## <a name="remarks"></a>Commenti

L'agente attività viene eseguito nella macchina virtuale quando tale macchina virtuale è pianificata per un aggiornamento del sistema. L'agente attività aggiorna la macchina virtuale quando viene [**chiamato il metodo StartTask.**](irdvtaskplugin-starttask.md)

Per registrare l'agente attività, aggiungere la chiave seguente al Registro di sistema della macchina virtuale:

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Terminal Server** \\ **Task** \\ **Plugins** \\ **TaskAgentName**

In questa chiave del Registro di sistema aggiungere i valori seguenti:



| Nome                     | Tipo                      | Descrizione                                                                   |
|--------------------------|---------------------------|-------------------------------------------------------------------------------|
| **Clsid**<br/>     | **REG \_ SZ**<br/>    | Stringa che rappresenta il **CLSID dell'agente** attività.<br/>          |
| **IsEnabled**<br/> | **REG \_ DWORD**<br/> | 0 se l'agente attività è disabilitato o 1 se l'agente attività è abilitato.<br/> |



 

> [!Note]  
> È possibile registrare più agenti attività, ma verrà utilizzato un solo agente attività. Se è abilitato più di un agente attività, verrà utilizzato solo il primo agente trovato.

 

Anche se questa interfaccia è supportata nei sistemi operativi identificati nei requisiti seguenti, verrà usata solo se la macchina virtuale è ospitata in Windows Server 2012.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------|
| Client minimo supportato<br/> | Windows 7 Enterprise<br/>   |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/> |



 

