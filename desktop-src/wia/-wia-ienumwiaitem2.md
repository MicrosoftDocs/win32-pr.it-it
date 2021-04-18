---
description: Utilizzato dalle applicazioni per enumerare gli oggetti IWiaItem2 nella cartella corrente dell'albero degli elementi.
ms.assetid: a82298e0-fbe7-4ef5-99c5-18ff60538e03
title: Interfaccia IEnumWiaItem2 (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: f6e41b3172793f696a9ea3c2d319bdee6ca3d691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308268"
---
# <a name="ienumwiaitem2-interface"></a>Interfaccia IEnumWiaItem2

Utilizzato dalle applicazioni per enumerare gli oggetti [**IWiaItem2**](-wia-iwiaitem2.md) nella cartella corrente dell'albero degli elementi.

## <a name="members"></a>Membri

L'interfaccia **IEnumWiaItem2** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IEnumWiaItem2** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IEnumWiaItem2** dispone di questi metodi.



| Metodo                                          | Descrizione                                                                                                                    |
|:------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**Clone**](-wia-ienumwiaitem2-clone.md)       | Crea un'istanza aggiuntiva dell'interfaccia **IEnumWiaItem2** e restituisce un puntatore. <br/>                  |
| [**GetCount**](-wia-ienumwiaitem2-getcount.md) | Restituisce il numero di elementi archiviati da questo enumeratore. <br/>                                                          |
| [**Avanti**](-wia-ienumwiaitem2-next.md)         | Riempie una matrice di puntatori alle interfacce [**IWiaItem2**](-wia-iwiaitem2.md) .<br/>                                       |
| [**Reset**](-wia-ienumwiaitem2-reset.md)       | Reimposta il riferimento di enumerazione sul primo oggetto [**IWiaItem2**](-wia-iwiaitem2.md) . <br/>                          |
| [**Ignora**](-wia-ienumwiaitem2-skip.md)         | Ignora il numero specificato di elementi durante un'enumerazione degli oggetti [**IWiaItem2**](-wia-iwiaitem2.md) disponibili.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
