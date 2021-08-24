---
description: I servizi di integrazione sono servizi software eseguiti sul sistema operativo guest all'interno di una macchina virtuale figlio e come parte dello stack di virtualizzazione nel sistema operativo di gestione per fornire un certo livello di integrazione con il sistema operativo di gestione.
ms.assetid: 7A8E9EF2-AC67-47CB-81A5-BF4C8A55D710
title: Classi di Integration Services
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e4d833263298b88872cbf6eda71b953798897f3ff820d0ae831b818b9c92eaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694401"
---
# <a name="integration-services-classes"></a>Classi di Integration Services

I servizi di integrazione sono servizi software eseguiti sul sistema operativo guest all'interno di una macchina virtuale figlio e come parte dello stack di virtualizzazione nel sistema operativo di gestione per fornire un certo livello di integrazione con il sistema operativo di gestione. Vengono usati per risolvere i problemi che derivano dall'elevato livello di isolamento fornito dalle macchine virtuali.

Di seguito sono riportate le classi WMI di virtualizzazione correlate ai servizi di integrazione.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                | Descrizione                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msvm \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)<br/>                                               | Rappresenta un processo dell'operazione del servizio file guest. <br/>                                                                                                                                                                                                            |
| [**Msvm \_ CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md)<br/>                               | Rappresenta i parametri per la copia di un file dall'host nel guest. <br/>                                                                                                                                                                                |
| [**Msvm \_ GuestFileService**](msvm-guestfileservice.md)<br/>                                                   | [**Msvm \_ GuestFileService contiene**](msvm-guestfileservice.md) un metodo che può essere usato per copiare un file in una macchina virtuale dall'host Hyper-V. <br/>                                                                                                     |
| [**Msvm \_ GuestService**](msvm-guestservice.md)<br/>                                                           | [**Msvm \_ GuestService**](msvm-guestservice.md) è la classe di base astratta per i servizi nel guest a cui è possibile accedere dall'host. <br/>                                                                                                                  |
| [**Msvm \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)<br/>                       | Rappresenta lo stato del componente dell'interfaccia del servizio guest, che fornisce un meccanismo per interagire con la macchina virtuale dalle interfacce di gestione nel sistema host. <br/>                                                                         |
| [**Msvm \_ GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md)<br/> | Rappresenta lo stato configurato del componente dell'interfaccia del servizio guest. <br/>                                                                                                                                                                                 |
| [**Msvm \_ KvpExchangeComponent**](msvm-kvpexchangecomponent.md)<br/>                                           | Rappresenta lo stato del servizio di scambio di coppie chiave/valore, che fornisce un meccanismo per lo scambio di dati tra la macchina virtuale e il sistema operativo in esecuzione nel sistema operativo di gestione.<br/>                                                  |
| [**Msvm \_ KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md)<br/>                     | Rappresenta lo stato configurato del servizio di scambio di coppie chiave/valore.<br/>                                                                                                                                                                                    |
| [**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)<br/>                                             | Rappresenta una coppia chiave/valore.<br/>                                                                                                                                                                                                                               |
| [**Msvm \_ RegisteredGuestService**](msvm-registeredguestservice.md)<br/>                                       | Rappresenta un'associazione tra un'istanza di [**Msvm \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) e un'istanza di [**Msvm \_ GuestService**](msvm-guestservice.md), che rappresenta un servizio in esecuzione nel guest. <br/> |
| [**Msvm \_ ShutdownComponent**](msvm-shutdowncomponent.md)<br/>                                                 | Rappresenta lo stato del servizio di arresto, che fornisce un meccanismo per arrestare il sistema operativo della macchina virtuale dalle interfacce di gestione nel sistema host.<br/>                                                                       |
| [**Msvm \_ ShutdownComponentSettingData**](msvm-shutdowncomponentsettingdata.md)<br/>                           | Rappresenta lo stato configurato del servizio di arresto.<br/>                                                                                                                                                                                                   |
| [**Msvm \_ TimeSyncComponent**](msvm-timesynccomponent.md)<br/>                                                 | Rappresenta lo stato del servizio di sincronizzazione dell'ora, responsabile della sincronizzazione dell'ora di sistema di una macchina virtuale con l'ora di sistema del sistema operativo in esecuzione nel sistema operativo di gestione.<br/>                             |
| [**Msvm \_ TimeSyncComponentSettingData**](msvm-timesynccomponentsettingdata.md)<br/>                           | Rappresenta lo stato configurato del servizio di sincronizzazione dell'ora.<br/>                                                                                                                                                                                       |
| [**Msvm \_ VssComponent**](msvm-vsscomponent.md)<br/>                                                           | Rappresenta lo stato del servizio Servizio Copia Shadow del volume (VSS), che implementa il richiedente vss nel sistema operativo guest.<br/>                                                                                                                    |
| [**Msvm \_ VssComponentSettingData**](msvm-vsscomponentsettingdata.md)<br/>                                     | Rappresenta lo stato configurato del servizio Servizio Copia Shadow del volume (VSS).<br/>                                                                                                                                                                           |



 

 

 




