---
title: Interfaccia IVMGuestOS (VPCCOMInterfaces.h)
description: Definisce il sistema operativo guest in esecuzione all'interno di una macchina virtuale.
ms.assetid: fb31f294-94ad-4545-8d59-849a5f2fe780
keywords:
- Interfaccia IVMGuestOS Virtual PC
- Interfaccia IVMGuestOS Virtual PC , descritto
topic_type:
- apiref
api_name:
- IVMGuestOS
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51a36c6c579209903c45e3888a11f17d40c168bbb2e215c60fb25e5b12330962
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593999"
---
# <a name="ivmguestos-interface"></a>Interfaccia IVMGuestOS

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definisce il sistema operativo guest in esecuzione all'interno di una macchina virtuale. Questa interfaccia consente di interagire con i componenti di integrazione in esecuzione all'interno del sistema operativo guest. **IVMGuestOS per** una macchina virtuale può essere recuperato usando la [**proprietà IVMVirtualMachine::GuestOS.**](ivmvirtualmachine-guestos.md)

## <a name="members"></a>Membri

**L'interfaccia IVMGuestOS** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMGuestOS** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia IVMGuestOS** include questi metodi.



| Metodo                                                                          | Descrizione                                                                                             |
|:--------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**GetOsVersionInfo**](ivmguestos-getosversioninfo.md)                         | Recupera le informazioni sulla versione per il sistema operativo guest in esecuzione nella macchina virtuale.<br/> |
| [**GetParameter**](ivmguestos-getparameter.md)                                 | Recupera un parametro denominato all'interno del guest.<br/>                                                |
| [**InstallIntegrationComponents**](ivmguestos-installintegrationcomponents.md) | Individua e installa i componenti di integrazione più recenti nel sistema operativo guest.<br/>      |
| [**IsUserLoggedOn**](ivmguestos-isuserloggedon.md)                             | Determina se la sessione richiesta è presente.<br/>                                         |
| [**Disconnessione**](ivmguestos-logoff.md)                                             | Disconnette tutti gli utenti dal sistema operativo guest.<br/>                                          |
| [**Riavvia**](ivmguestos-restart.md)                                           | Riavvia il sistema operativo guest.<br/>                                                         |
| [**SetParameter**](ivmguestos-setparameter.md)                                 | Imposta un parametro denominato all'interno del guest.<br/>                                                     |
| [**Arresto**](ivmguestos-shutdown.md)                                         | Arresta il sistema operativo guest.<br/>                                                       |



 

### <a name="properties"></a>Proprietà

Queste proprietà sono disponibili nell'interfaccia **IVMGuestOS.**



| Proprietà                                                                                   | Tipo di accesso           | Descrizione                                                                                                                                 |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanShutdown**](ivmguestos-canshutdown.md)<br/>                                   | Sola lettura<br/>  | Indica se il sistema operativo guest può essere arrestato in modo pulito (richiede componenti di integrazione).<br/>                         |
| [**Nomecomputer**](ivmguestos-computername.md)<br/>                                 | Sola lettura<br/>  | Nome computer del sistema operativo guest in esecuzione nella macchina virtuale.<br/>                                                  |
| [**CSDVersion**](ivmguestos-csdversion.md)<br/>                                     | Sola lettura<br/>  | CSDVersion del sistema operativo guest in esecuzione nella macchina virtuale.<br/>                                                     |
| [**HeartbeatPercentage**](ivmguestos-heartbeatpercentage.md)<br/>                   | Sola lettura<br/>  | Percentuale di heartbeat previsti ricevuti nell'ultimo minuto.<br/>                                                             |
| [**IntegrationComponentsVersion**](ivmguestos-integrationcomponentsversion.md)<br/> | Sola lettura<br/>  | Versione dei componenti di integrazione installati nel sistema operativo guest.<br/>                                               |
| [**IsAssbeating**](ivmguestos-isheartbeating.md)<br/>                             | Sola lettura<br/>  | Indica se la macchina virtuale ha un heartbeat.<br/>                                                                           |
| [**IsHostTimeSyncEnabled**](ivmguestos-ishosttimesyncenabled.md)<br/>               | Lettura/Scrittura<br/> | Indica se i componenti di integrazione in questa macchina virtuale devono sincronizzare l'orologio del guest con l'orologio dell'host.<br/> |
| [**MultipleUserSessionsAllowed**](ivmguestos-multipleusersessionsallowed.md)<br/>   | Sola lettura<br/>  | Indica se nel sistema operativo guest sono consentite più sessioni utente simultanee.<br/>                                 |
| [**OSBuildNumber**](ivmguestos-osbuildnumber.md)<br/>                               | Sola lettura<br/>  | Numero di build del sistema operativo guest in esecuzione nella macchina virtuale.<br/>                                                   |
| [**OSMajorVersion**](ivmguestos-osmajorversion.md)<br/>                             | Sola lettura<br/>  | Versione principale del sistema operativo guest in esecuzione nella macchina virtuale.<br/>                                                  |
| [**OSMinorVersion**](ivmguestos-osminorversion.md)<br/>                             | Sola lettura<br/>  | Versione secondaria del sistema operativo guest in esecuzione nella macchina virtuale.<br/>                                                  |
| [**OSName**](ivmguestos-osname.md)<br/>                                             | Sola lettura<br/>  | Nome del sistema operativo guest in esecuzione nella macchina virtuale.<br/>                                                           |
| [**OSPlatformId**](ivmguestos-osplatformid.md)<br/>                                 | Sola lettura<br/>  | Identificatore di piattaforma del sistema operativo guest in esecuzione nella macchina virtuale.<br/>                                            |
| [**OSVersion**](ivmguestos-osversion.md)<br/>                                       | Sola lettura<br/>  | Versione del sistema operativo guest in esecuzione nella macchina virtuale.<br/>                                                        |
| [**ProductType**](ivmguestos-producttype.md)<br/>                                   | Sola lettura<br/>  | Tipo di prodotto del sistema operativo guest in esecuzione nella macchina virtuale.<br/>                                                   |
| [**ScreenLocked**](ivmguestos-screenlocked.md)<br/>                                 | Sola lettura<br/>  | Indica se lo schermo è bloccato nel sistema operativo guest.<br/>                                                            |
| [**ServicePackMajor**](ivmguestos-servicepackmajor.md)<br/>                         | Sola lettura<br/>  | Versione principale del Service Pack del sistema operativo guest in esecuzione nella macchina virtuale.<br/>                              |
| [**ServicePackMinor**](ivmguestos-servicepackminor.md)<br/>                         | Sola lettura<br/>  | Versione secondaria del Service Pack del sistema operativo guest in esecuzione nella macchina virtuale.<br/>                              |
| [**SuiteMask**](ivmguestos-suitemask.md)<br/>                                       | Sola lettura<br/>  | SuiteMask del sistema operativo guest in esecuzione nella macchina virtuale.<br/>                                                      |
| [**TerminalServerPort**](ivmguestos-terminalserverport.md)<br/>                     | Sola lettura<br/>  | La porta usata Servizi Desktop remoto nel sistema operativo guest.<br/>                                                              |
| [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md)<br/>   | Sola lettura<br/>  | Stato dell'inizializzazione di Servizi terminal nel sistema operativo guest.<br/>                                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



 

