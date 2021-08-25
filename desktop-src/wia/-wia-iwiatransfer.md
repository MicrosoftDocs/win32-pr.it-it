---
description: L'interfaccia IWiaTransfer fornisce il trasferimento dei dati basato su flusso.
ms.assetid: 7bc6d3b8-9bf0-4b77-aa2b-b7c64c5730c0
title: Interfaccia IWiaTransfer (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: ff19619b1f0ab46658d0876792248befd6940c525d5c7da1b3331f6ca1a8c12e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813901"
---
# <a name="iwiatransfer-interface"></a>Interfaccia IWiaTransfer

**L'interfaccia IWiaTransfer** fornisce il trasferimento dei dati basato su flusso.

## <a name="members"></a>Membri

**L'interfaccia IWiaTransfer** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaTransfer** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IWiaTransfer.**



| Metodo                                                                 | Descrizione                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Annulla**](-wia-iwiatransfer-cancel.md)                             | Annulla l'operazione di trasferimento corrente. <br/>                                         |
| [**Scarica**](-wia-iwiatransfer-download.md)                         | Avvia un download di dati nel chiamante. <br/>                                        |
| [**EnumWIA \_ FORMAT \_ INFO**](-wia-iwiatransfer-enumwia-format-info.md) | Crea un enumeratore per i formati di trasferimento supportati dal dispositivo WIA 2.0.<br/> |
| [**Caricamento**](-wia-iwiatransfer-upload.md)                             | Avvia un caricamento dei dati di un singolo elemento dal chiamante. <br/>                       |



 

## <a name="remarks"></a>Commenti

**L'interfaccia IWiaTransfer,** come tutte le Component Object Model (COM), eredita i [metodi dell'interfaccia IUnknown.](/windows/win32/api/unknwn/nn-unknwn-iunknown)



| Metodi IUnknown                                        | Descrizione                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Restituisce puntatori alle interfacce supportate. |
| [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa il conteggio dei riferimenti.               |
| [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Riduce il conteggio dei riferimenti.               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
