---
title: Interfaccia INapSoHProcessor (NapProtocol.h)
description: Vengono usati dagli SHA per elaborare il contenuto di SoHResponses e dagli SHV per elaborare il contenuto di SoHRequests.
ms.assetid: c2dd71ca-a4dd-44d2-81ab-b83e90599a2f
keywords:
- Interfaccia INapSoHProcessor NAP
- Interfaccia INapSoHProcessor nap , descritta
topic_type:
- apiref
api_name:
- INapSoHProcessor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca4a87e15d3810605038231eaec066e9f26ed079aca0d0715c72e7c69ed8d600
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799483"
---
# <a name="inapsohprocessor-interface"></a>Interfaccia INapSoHProcessor

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

**INapSoHProcessor** fornisce metodi usati dagli SHA per elaborare il contenuto di [**SoHResponses**](/windows/win32/api/naptypes/ns-naptypes-soh) e dagli SHV per elaborare il contenuto di **SoHRequests.**

## <a name="members"></a>Membri

**L'interfaccia INapSoHProcessor** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapSoHProcessor** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia INapSoHProcessor** include questi metodi.



| Metodo                                                                                           | Descrizione                                                                           |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**INapSoHProcessor::FindNextAttribute**](inapsohprocessor-findnextattribute-method.md)         | Trova l'indice di posizione dell'attributo del pacchetto SoH successivo.<br/>                 |
| [**INapSoHProcessor::GetAttribute**](inapsohprocessor-getattribute-method.md)                   | Recupera il tipo e il valore dell'attributo.<br/>                                    |
| [**INapSoHProcessor::GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md) | Recupera il numero di attributi contenuti in SoH.<br/>                   |
| [**INapSoHProcessor::Initialize**](inapsohprocessor-initialize-method.md)                       | Inizializza il pacchetto del protocollo SoH e il sistema di protezione accesso alla rete per l'elaborazione del contenuto.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce di Protezione accesso alla rete](nap-interfaces.md)
</dt> <dt>

[Informazioni di riferimento su Protezione accesso alla rete](nap-reference.md)
</dt> </dl>

 

