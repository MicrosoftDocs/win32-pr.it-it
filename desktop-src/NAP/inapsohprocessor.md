---
title: Interfaccia INapSoHProcessor (NapProtocol. h)
description: Vengono usati da SHAs per elaborare il contenuto di SoHResponses e SHV per elaborare il contenuto di SoHRequests.
ms.assetid: c2dd71ca-a4dd-44d2-81ab-b83e90599a2f
keywords:
- NAP interfaccia INapSoHProcessor
- Interfaccia NAP di INapSoHProcessor, descrizione
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
ms.openlocfilehash: 1c43abf137bb267468deeb9d4bd47546275ba6c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047888"
---
# <a name="inapsohprocessor-interface"></a>Interfaccia INapSoHProcessor

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

**INapSoHProcessor** fornisce i metodi usati da Shas per elaborare il contenuto di [**SoHResponses**](/windows/win32/api/naptypes/ns-naptypes-soh) e SHV per elaborare il contenuto di **SoHRequests**.

## <a name="members"></a>Membri

L'interfaccia **INapSoHProcessor** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSoHProcessor** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **INapSoHProcessor** dispone di questi metodi.



| Metodo                                                                                           | Descrizione                                                                           |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**INapSoHProcessor::FindNextAttribute**](inapsohprocessor-findnextattribute-method.md)         | Trova l'indice della posizione dell'attributo del pacchetto di rapporto di integrità successivo.<br/>                 |
| [**INapSoHProcessor:: GetAttribute**](inapsohprocessor-getattribute-method.md)                   | Recupera il tipo e il valore dell'attributo.<br/>                                    |
| [**INapSoHProcessor::GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md) | Recupera il numero di attributi contenuti nel rapporto di integrità.<br/>                   |
| [**INapSoHProcessor:: Initialize**](inapsohprocessor-initialize-method.md)                       | Inizializza il pacchetto del protocollo di rapporto di integrità e il sistema NAP per l'elaborazione del contenuto.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce NAP](nap-interfaces.md)
</dt> <dt>

[Riferimento NAP](nap-reference.md)
</dt> </dl>

 

