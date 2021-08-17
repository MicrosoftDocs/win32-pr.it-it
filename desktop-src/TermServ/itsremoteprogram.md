---
title: Interfaccia ITSRemoteProgram
description: Include metodi per impostare e recuperare la modalità RemoteApp e i parametri di avvio per un programma RemoteApp, ad esempio il percorso del file eseguibile e la directory di lavoro.
ms.assetid: c9eec63b-7162-4bf8-b5d5-8cadb971ef98
ms.tgt_platform: multiple
keywords:
- Interfaccia ITSRemoteProgram Servizi Desktop remoto
- Interfaccia ITSRemoteProgram Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- ITSRemoteProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b719771f265347da59ce4d8c5990a5b9dc5a72315780def0fd3a34b108e18169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756810"
---
# <a name="itsremoteprogram-interface"></a>Interfaccia ITSRemoteProgram

Include metodi per impostare e recuperare la modalità RemoteApp e i parametri di avvio per un programma RemoteApp, ad esempio il percorso del file eseguibile e la directory di lavoro.

## <a name="members"></a>Membri

**L'interfaccia ITSRemoteProgram** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITSRemoteProgram** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia ITSRemoteProgram** include questi metodi.



| Metodo                                                            | Descrizione                                                              |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**ServerStartProgram**](itsremoteprogram-serverstartprogram.md) | Specifica un programma RemoteApp da avviare nella sessione remota.<br/> |



 

### <a name="properties"></a>Proprietà

**L'interfaccia ITSRemoteProgram** ha queste proprietà.



| Proprietà                                                                   | Tipo di accesso           | Descrizione                    |
|:---------------------------------------------------------------------------|:----------------------|:-------------------------------|
| [**RemoteProgramMode**](itsremoteprogram-remoteprogrammode.md)<br/> | Lettura/Scrittura<br/> | Modalità RemoteApp.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID ITSRemoteProgram è definito \_ come FDD029F9-467A-4c49-8529-64B521DBD1B4<br/>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Idispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Connessione Web Desktop remoto riferimento](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

