---
title: Interfaccia INapSoHConstructor (NapProtocol. h)
description: Vengono usati da SHAs per costruire SoHRequests e SHV per costruire SoHResponses.
ms.assetid: ad79c80a-3003-4465-b350-77890c217d63
keywords:
- NAP interfaccia INapSoHConstructor
- Interfaccia NAP di INapSoHConstructor, descrizione
topic_type:
- apiref
api_name:
- INapSoHConstructor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 546a6d3b4ec262fdd725af24211338e848b2b848
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963821"
---
# <a name="inapsohconstructor-interface"></a>Interfaccia INapSoHConstructor

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

**INapSoHConstructor** fornisce i metodi usati da Shas per costruire [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) e SHV per costruire **SoHResponses**.

## <a name="members"></a>Membri

L'interfaccia **INapSoHConstructor** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSoHConstructor** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **INapSoHConstructor** dispone di questi metodi.



| Metodo                                                                                   | Descrizione                                         |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------|
| [**INapSoHConstructor:: AppendAttribute**](inapsohconstructor-appendattribute-method.md) | Aggiunge un TLV alla fine del buffer del rapporto di integrità.<br/> |
| [**INapSoHConstructor::GetSoH**](inapsohconstructor-getsoh-method.md)                   | Recupera il pacchetto SoH costruito.<br/>    |
| [**INapSoHConstructor:: Initialize**](inapsohconstructor-initialize-method.md)           | Inizializza il pacchetto SoH.<br/>              |
| [**INapSoHConstructor:: Validate**](inapsohconstructor-validate-method.md)               | Verifica la validità del pacchetto SoH.<br/>   |



 

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

 

