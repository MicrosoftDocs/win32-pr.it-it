---
description: Tipi di enumerazione utilizzati con la gestione del disco.
ms.assetid: ed8fe5c1-dbdf-43bc-a0a7-17e541eba950
title: Tipi di enumerazione di Gestione disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e850e5161e4e8a6326d8014f67d6aad9373015e4354a01fa353087c6863a39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765911"
---
# <a name="disk-management-enumeration-types"></a>Tipi di enumerazione di Gestione disco

I tipi di enumerazione seguenti vengono usati con la gestione del disco.

## <a name="in-this-section"></a>Contenuto della sezione



| Enumerazione                                                                              | Descrizione                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPO DI \_ SUPPORTO**](/windows/win32/api/winioctl/ne-winioctl-media_type)<br/>                                         | Rappresenta i vari formati di supporto del dispositivo.<br/>                                                                                                                                                                                                                                                             |
| [**STILE \_ PARTIZIONE**](/windows/win32/api/winioctl/ne-winioctl-partition_style)<br/>                               | Rappresenta il formato di una partizione.<br/>                                                                                                                                                                                                                                                                     |
| [**TIPO DI \_ BUS DI \_ ARCHIVIAZIONE**](/windows/win32/api/winioctl/ne-winioctl-storage_bus_type)<br/>                                | Fornisce un mezzo simbolico per rappresentare i tipi di bus di archiviazione.<br/>                                                                                                                                                                                                                                              |
| [**STATO DI \_ INTEGRITÀ DEL COMPONENTE DI \_ \_ ARCHIVIAZIONE**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_component_health_status)<br/> | Specifica lo stato di integrità di un componente di archiviazione.<br/>                                                                                                                                                                                                                                                       |
| [**FATTORE \_ DI FORMA DEL DISPOSITIVO DI \_ \_ ARCHIVIAZIONE**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_device_form_factor)<br/>           | Specifica il fattore di forma di un dispositivo.<br/>                                                                                                                                                                                                                                                                    |
| [**UNITÀ POWER \_ CAP DEL DISPOSITIVO DI \_ \_ \_ ARCHIVIAZIONE**](/windows/desktop/api/winioctl/ne-winioctl-storage_device_power_cap_units)<br/>  | Unità della soglia di potenza massima.<br/>                                                                                                                                                                                                                                                                 |
| [**SET DI \_ CODICI \_ PORTA DI \_ ARCHIVIAZIONE**](/windows/win32/api/winioctl/ne-winioctl-storage_port_code_set)<br/>                     | Riservato per l'utilizzo nel sistema. <br/>                                                                                                                                                                                                                                                                                 |
| [**ID PROPRIETÀ \_ DI \_ ARCHIVIAZIONE**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id)<br/>                          | Enumera i valori possibili del membro **PropertyId** della struttura [**STORAGE PROPERTY \_ \_ QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) passata come input alla richiesta [**IOCTL \_ STORAGE QUERY \_ \_ PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) per recuperare le proprietà di un dispositivo di archiviazione o di un adattatore.<br/> |
| [**TIPO \_ DI PROTOCOLLO DI \_ ARCHIVIAZIONE**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_type)<br/>                      | Specifica il protocollo di un dispositivo di archiviazione.<br/>                                                                                                                                                                                                                                                               |
| [**TIPO \_ DI QUERY DI \_ ARCHIVIAZIONE**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_query_type)<br/>                            | Usato dalla struttura [**QUERY \_ STORAGE \_ PROPERTY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) passata al codice di controllo [**IOCTL \_ STORAGE QUERY \_ \_ PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) per indicare quali informazioni vengono restituite su una proprietà di un dispositivo di archiviazione o di un adattatore.<br/>                             |
| [**WRITE \_ CACHE \_ CHANGE**](/windows/win32/api/winioctl/ne-winioctl-write_cache_change)<br/>                            | Indica se le funzionalità della cache di scrittura di un dispositivo sono modificabili.<br/>                                                                                                                                                                                                                                    |
| [**WRITE \_ CACHE \_ ENABLE**](/windows/win32/api/winioctl/ne-winioctl-write_cache_enable)<br/>                            | Indica se la cache di scrittura è abilitata o disabilitata.<br/>                                                                                                                                                                                                                                                 |
| [**TIPO \_ DI CACHE DI \_ SCRITTURA**](/windows/win32/api/winioctl/ne-winioctl-write_cache_type)<br/>                                | Specifica il tipo di cache.<br/>                                                                                                                                                                                                                                                                                 |
| [**WRITE \_ THROUGH**](/windows/win32/api/winioctl/ne-winioctl-write_through)<br/>                                       | Specifica se un dispositivo di archiviazione supporta la memorizzazione nella cache write-through.<br/>                                                                                                                                                                                                                                        |



 

 

