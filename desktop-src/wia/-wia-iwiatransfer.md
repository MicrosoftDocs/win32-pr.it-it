---
description: L'interfaccia IWiaTransfer fornisce il trasferimento dei dati basato sul flusso.
ms.assetid: 7bc6d3b8-9bf0-4b77-aa2b-b7c64c5730c0
title: Interfaccia IWiaTransfer (WIA. h)
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
ms.openlocfilehash: 623cc21591289f4c1fff33cabe1d504b3682708c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226145"
---
# <a name="iwiatransfer-interface"></a>Interfaccia IWiaTransfer

L'interfaccia **IWiaTransfer** fornisce il trasferimento dei dati basato sul flusso.

## <a name="members"></a>Membri

L'interfaccia **IWiaTransfer** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaTransfer** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWiaTransfer** dispone di questi metodi.



| Metodo                                                                 | Descrizione                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Annulla**](-wia-iwiatransfer-cancel.md)                             | Annulla l'operazione di trasferimento corrente. <br/>                                         |
| [**Scarica**](-wia-iwiatransfer-download.md)                         | Avvia un download di dati al chiamante. <br/>                                        |
| [**\_Informazioni sul formato EnumWIA \_**](-wia-iwiatransfer-enumwia-format-info.md) | Crea un enumeratore per i formati di trasferimento supportati dal dispositivo WIA 2,0.<br/> |
| [**Carica**](-wia-iwiatransfer-upload.md)                             | Avvia un caricamento di dati di un singolo elemento dal chiamante. <br/>                       |



 

## <a name="remarks"></a>Commenti

L'interfaccia **IWiaTransfer** , come tutte le interfacce Component Object Model (com), eredita i metodi di interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



| Metodi IUnknown                                        | Descrizione                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Restituisce puntatori alle interfacce supportate. |
| [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa il conteggio dei riferimenti.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Riduce il conteggio dei riferimenti.               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
