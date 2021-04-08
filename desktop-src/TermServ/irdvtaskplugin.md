---
title: Interfaccia IRDVTaskPlugin
description: L'interfaccia IRDVTaskPlugin viene implementata da un agente attività aggiornamento macchina virtuale per consentire all'agente attività di gestire gli aggiornamenti del sistema per una macchina virtuale.
ms.assetid: e06eb707-be78-4d1f-96d3-21526b167e61
ms.tgt_platform: multiple
keywords:
- Interfaccia IRDVTaskPlugin Servizi Desktop remoto
- Interfaccia IRDVTaskPlugin Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IRDVTaskPlugin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59e90e899e8084f7fbc6b0b6f11067061eaa807b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964905"
---
# <a name="irdvtaskplugin-interface"></a>Interfaccia IRDVTaskPlugin

L'interfaccia **IRDVTaskPlugin** viene implementata da un *agente attività* aggiornamento macchina virtuale per consentire all'agente attività di gestire gli aggiornamenti del sistema per una macchina virtuale. Questa interfaccia viene utilizzata dall' *agente trigger*, che viene implementato dal sistema host.

## <a name="members"></a>Membri

L'interfaccia **IRDVTaskPlugin** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IRDVTaskPlugin** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IRDVTaskPlugin** dispone di questi metodi.



| Metodo                                          | Descrizione                                                        |
|:------------------------------------------------|:-------------------------------------------------------------------|
| [**Inizializzare**](irdvtaskplugin-initialize.md) | Chiamato per inizializzare l'agente attività.<br/>                    |
| [**StartTask**](irdvtaskplugin-starttask.md)   | Chiamato per avviare l'attività di aggiornamento nella macchina virtuale.<br/> |
| [**Terminare**](irdvtaskplugin-terminate.md)   | Chiamato quando l'agente attività viene arrestato.<br/>          |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IRDVTaskPlugin** ha queste proprietà.



| Proprietà                                                   | Tipo di accesso          | Descrizione                                             |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------|
| [**PluginName**](irdvtaskplugin-pluginname.md)<br/> | Sola lettura<br/> | Contiene il nome visualizzato dell'agente attività.<br/> |



 

## <a name="remarks"></a>Commenti

L'agente attività viene eseguito nella macchina virtuale quando la macchina virtuale è pianificata per un aggiornamento del sistema. L'agente attività Aggiorna la macchina virtuale quando viene chiamato il metodo [**StartTask**](irdvtaskplugin-starttask.md) .

Per registrare l'agente attività, aggiungere la chiave seguente al registro di sistema della macchina virtuale:

**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Terminal Server** \\  \\ **plugin** attività \\ **TaskAgentName**

In questa chiave del registro di sistema aggiungere i valori seguenti:



| Nome                     | Tipo                      | Descrizione                                                                   |
|--------------------------|---------------------------|-------------------------------------------------------------------------------|
| **CLSID**<br/>     | **REG \_ SZ**<br/>    | Stringa che rappresenta il **CLSID** dell'agente attività.<br/>          |
| **IsEnabled**<br/> | **REG \_ DWORD**<br/> | 0 se l'agente attività è disabilitato o 1 se l'agente attività è abilitato.<br/> |



 

> [!Note]  
> È possibile registrare più di un agente attività, ma verrà usato un solo agente attività. Se è abilitato più di un agente attività, verrà utilizzato solo il primo oggetto trovato.

 

Sebbene questa interfaccia sia supportata nei sistemi operativi indicati nei requisiti indicati di seguito, verrà usata solo se la macchina virtuale è ospitata in Windows Server 2012.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------|
| Client minimo supportato<br/> | Windows 7 Enterprise<br/>   |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/> |



 

