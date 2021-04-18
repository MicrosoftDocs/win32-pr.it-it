---
description: Tipi di enumerazione usati con Gestione disco.
ms.assetid: ed8fe5c1-dbdf-43bc-a0a7-17e541eba950
title: Tipi di enumerazione di gestione disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c186a2a722bf9614bb83b19bcaa29be486cf54bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316777"
---
# <a name="disk-management-enumeration-types"></a>Tipi di enumerazione di gestione disco

I tipi di enumerazione seguenti vengono utilizzati con Gestione disco.

## <a name="in-this-section"></a>Contenuto della sezione



| Enumerazione                                                                              | Descrizione                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**tipo di supporto \_**](/windows/win32/api/winioctl/ne-winioctl-media_type)<br/>                                         | Rappresenta le varie forme di supporti del dispositivo.<br/>                                                                                                                                                                                                                                                             |
| [**\_stile partizione**](/windows/win32/api/winioctl/ne-winioctl-partition_style)<br/>                               | Rappresenta il formato di una partizione.<br/>                                                                                                                                                                                                                                                                     |
| [**\_tipo di bus di archiviazione \_**](/windows/win32/api/winioctl/ne-winioctl-storage_bus_type)<br/>                                | Fornisce un mezzo simbolico per rappresentare i tipi di bus di archiviazione.<br/>                                                                                                                                                                                                                                              |
| [**\_stato di \_ integrità del componente di archiviazione \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_component_health_status)<br/> | Specifica lo stato di integrità di un componente di archiviazione.<br/>                                                                                                                                                                                                                                                       |
| [**\_fattore di \_ forma del dispositivo di archiviazione \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_device_form_factor)<br/>           | Specifica il fattore di forma di un dispositivo.<br/>                                                                                                                                                                                                                                                                    |
| [**\_unità di \_ alimentazione del dispositivo \_ di archiviazione \_**](/windows/desktop/api/winioctl/ne-winioctl-storage_device_power_cap_units)<br/>  | Unità della soglia di potenza massima.<br/>                                                                                                                                                                                                                                                                 |
| [**\_set di \_ codici \_ porta di archiviazione**](/windows/win32/api/winioctl/ne-winioctl-storage_port_code_set)<br/>                     | Riservato per l'utilizzo nel sistema. <br/>                                                                                                                                                                                                                                                                                 |
| [**\_ID proprietà di archiviazione \_**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id)<br/>                          | Enumera i possibili valori del membro **PropertyId** della struttura della [**query della \_ proprietà \_ di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) passata come input alla richiesta [**della \_ \_ \_ proprietà di query di archiviazione IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) per recuperare le proprietà di un dispositivo o di un adattatore di archiviazione.<br/> |
| [**\_tipo di protocollo di archiviazione \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_type)<br/>                      | Specifica il protocollo di un dispositivo di archiviazione.<br/>                                                                                                                                                                                                                                                               |
| [**\_tipo di query di archiviazione \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_query_type)<br/>                            | Usato dalla struttura [**di \_ \_ query della proprietà di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) passata al codice di controllo della [**\_ \_ \_ proprietà di query di archiviazione IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) per indicare quali informazioni vengono restituite su una proprietà di un dispositivo o di un adattatore di archiviazione.<br/>                             |
| [**\_modifica cache di scrittura \_**](/windows/win32/api/winioctl/ne-winioctl-write_cache_change)<br/>                            | Indica se le funzionalità della cache di scrittura di un dispositivo sono modificabili.<br/>                                                                                                                                                                                                                                    |
| [**\_Abilita cache di scrittura \_**](/windows/win32/api/winioctl/ne-winioctl-write_cache_enable)<br/>                            | Indica se la cache di scrittura è abilitata o disabilitata.<br/>                                                                                                                                                                                                                                                 |
| [**Scrivi \_ tipo di cache \_**](/windows/win32/api/winioctl/ne-winioctl-write_cache_type)<br/>                                | Specifica il tipo di cache.<br/>                                                                                                                                                                                                                                                                                 |
| [**Scrivi \_ attraverso**](/windows/win32/api/winioctl/ne-winioctl-write_through)<br/>                                       | Specifica se un dispositivo di archiviazione supporta la memorizzazione nella cache write-through.<br/>                                                                                                                                                                                                                                        |



 

 

