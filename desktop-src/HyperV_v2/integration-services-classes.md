---
description: I servizi di integrazione sono servizi software eseguiti sopra il sistema operativo guest all'interno di una macchina virtuale figlio e come parte dello stack di virtualizzazione nel sistema operativo di gestione per fornire un certo livello di integrazione con il sistema operativo di gestione.
ms.assetid: 7A8E9EF2-AC67-47CB-81A5-BF4C8A55D710
title: Classi di Integration Services
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04d60a913159c49387848b5e18a3e37b942f3e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528201"
---
# <a name="integration-services-classes"></a>Classi di Integration Services

I servizi di integrazione sono servizi software eseguiti sopra il sistema operativo guest all'interno di una macchina virtuale figlio e come parte dello stack di virtualizzazione nel sistema operativo di gestione per fornire un certo livello di integrazione con il sistema operativo di gestione. Vengono usati per risolvere i problemi che derivano dall'elevato livello di isolamento fornito dalle macchine virtuali.

Di seguito sono riportate le classi WMI di virtualizzazione correlate ai servizi di integrazione.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                | Descrizione                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CopyFileToGuestJob MSVM**](msvm-copyfiletoguestjob.md)<br/>                                               | Rappresenta un processo di operazione del servizio file Guest. <br/>                                                                                                                                                                                                            |
| [**\_CopyFileToGuestSettingData MSVM**](msvm-copyfiletoguestsettingdata.md)<br/>                               | Rappresenta i parametri per la copia di un file dall'host nel guest. <br/>                                                                                                                                                                                |
| [**\_GuestFileService MSVM**](msvm-guestfileservice.md)<br/>                                                   | [**MSVM \_ GuestFileService**](msvm-guestfileservice.md) contiene un metodo che può essere utilizzato per copiare un file in una macchina virtuale dall'host Hyper-V. <br/>                                                                                                     |
| [**\_GuestService MSVM**](msvm-guestservice.md)<br/>                                                           | [**MSVM \_ GuestService**](msvm-guestservice.md) è la classe di base astratta per i servizi nel Guest a cui è possibile accedere dall'host. <br/>                                                                                                                  |
| [**\_GuestServiceInterfaceComponent MSVM**](msvm-guestserviceinterfacecomponent.md)<br/>                       | Rappresenta lo stato del componente dell'interfaccia del servizio Guest, che fornisce un meccanismo per interagire con la macchina virtuale dalle interfacce di gestione nel sistema host. <br/>                                                                         |
| [**\_GuestServiceInterfaceComponentSettingData MSVM**](msvm-guestserviceinterfacecomponentsettingdata.md)<br/> | Rappresenta lo stato configurato del componente dell'interfaccia del servizio Guest. <br/>                                                                                                                                                                                 |
| [**\_KvpExchangeComponent MSVM**](msvm-kvpexchangecomponent.md)<br/>                                           | Rappresenta lo stato del servizio di scambio di coppie chiave/valore, che fornisce un meccanismo per lo scambio di dati tra la macchina virtuale e il sistema operativo in esecuzione nel sistema operativo di gestione.<br/>                                                  |
| [**\_KvpExchangeComponentSettingData MSVM**](msvm-kvpexchangecomponentsettingdata.md)<br/>                     | Rappresenta lo stato configurato del servizio di scambio di coppie chiave/valore.<br/>                                                                                                                                                                                    |
| [**\_KvpExchangeDataItem MSVM**](msvm-kvpexchangedataitem.md)<br/>                                             | Rappresenta una coppia chiave/valore.<br/>                                                                                                                                                                                                                               |
| [**\_RegisteredGuestService MSVM**](msvm-registeredguestservice.md)<br/>                                       | Rappresenta un'associazione tra un'istanza di [**MSVM \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) e un'istanza di [**MSVM \_ GuestService**](msvm-guestservice.md), che rappresenta un servizio in esecuzione nel guest. <br/> |
| [**\_ShutdownComponent MSVM**](msvm-shutdowncomponent.md)<br/>                                                 | Rappresenta lo stato del servizio di arresto, che fornisce un meccanismo per arrestare il sistema operativo della macchina virtuale dalle interfacce di gestione nel sistema host.<br/>                                                                       |
| [**\_ShutdownComponentSettingData MSVM**](msvm-shutdowncomponentsettingdata.md)<br/>                           | Rappresenta lo stato configurato del servizio di arresto.<br/>                                                                                                                                                                                                   |
| [**\_TimeSyncComponent MSVM**](msvm-timesynccomponent.md)<br/>                                                 | Rappresenta lo stato del servizio di sincronizzazione dell'ora, che è responsabile della sincronizzazione dell'ora di sistema di una macchina virtuale con l'ora di sistema del sistema operativo in esecuzione nel sistema operativo di gestione.<br/>                             |
| [**\_TimeSyncComponentSettingData MSVM**](msvm-timesynccomponentsettingdata.md)<br/>                           | Rappresenta lo stato configurato del servizio di sincronizzazione dell'ora.<br/>                                                                                                                                                                                       |
| [**\_VssComponent MSVM**](msvm-vsscomponent.md)<br/>                                                           | Rappresenta lo stato del servizio di Servizio Copia Shadow del volume (VSS), che implementa il richiedente del servizio Copia Shadow del volume nel sistema operativo guest.<br/>                                                                                                                    |
| [**\_VssComponentSettingData MSVM**](msvm-vsscomponentsettingdata.md)<br/>                                     | Rappresenta lo stato configurato del servizio Servizio Copia Shadow del volume (VSS).<br/>                                                                                                                                                                           |



 

 

 




