---
description: Fornisce i metodi necessari per costruire e gestire un'smart card di dati del protocollo applicativo (APDU, Application Protocol Data Unit).
ms.assetid: fd84bb2e-27da-4670-b8e8-56c7948b78bb
title: Interfaccia ISCardCmd (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd
- ISCardCmd.Type
- ISCardCmd.get_Type
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e6bce160cfb326f0c44b2fca1c6676b895d9eeeec434826d7fc595fc178c47d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008148"
---
# <a name="iscardcmd-interface"></a>Interfaccia ISCardCmd

\[**L'interfaccia ISCardCmd** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

**L'interfaccia ISCardCmd** fornisce i metodi necessari per costruire e gestire un'smart card di dati del protocollo [](../secgloss/s-gly.md) [*applicativo*](../secgloss/a-gly.md) (APDU). Questa interfaccia incapsula due buffer:

-   Il buffer APDU contiene la sequenza di comando che verrà inviata alla scheda.
-   Il buffer APDUReply contiene i dati restituiti dalla scheda dopo l'esecuzione del comando APDU (questi dati sono definiti anche APDU restituiti).

L'esempio seguente illustra un uso tipico **dell'interfaccia ISCardCmd.** **L'interfaccia ISCardCmd** viene usata per creare un'APDU.

**Per inviare una transazione a una scheda specifica**

1.  Creare [**un'interfaccia ISCard**](iscard.md) e connettersi a un smart card.
2.  Creare **un'interfaccia ISCardCmd.**
3.  Compilare smart card comando APDU usando [**l'interfaccia ISCardISO7816**](iscardiso7816.md) o uno dei metodi di compilazione **ISCardCmd.**
4.  Eseguire il comando sul smart card chiamando il metodo di [**interfaccia ISCard**](iscard.md) appropriato.
5.  Valutare la risposta restituita.
6.  Ripetere la procedura in base alle esigenze.
7.  Rilasciare **l'interfaccia ISCardCmd** e altre interfacce in base alle esigenze.

## <a name="members"></a>Membri

**L'interfaccia ISCardCmd** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardCmd** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia ISCardCmd** include questi metodi.



| Metodo                                       | Descrizione                                                                                                |
|:---------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**BuildCmd**](iscardcmd-buildcmd.md)       | Costruisce un comando APDU valido per la trasmissione a un smart card.<br/>                               |
| [**Cancella**](iscardcmd-clear.md)             | Cancella i buffer dei messaggi APDU e APDU di risposta.<br/>                                             |
| [**Incapsulare**](iscardcmd-encapsulate.md) | Incapsula l'APDU del comando specificato in un altro comando APDU per la trasmissione a un smart card.<br/> |



 

### <a name="properties"></a>Proprietà

Queste proprietà sono disponibili nell'interfaccia **ISCardCmd.**



| Proprietà                                                              | Tipo di accesso           | Descrizione                                                                                                                                                         |
|:----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AlternateClassId**](iscardcmd-get-alternateclassid.md)<br/> | Lettura/Scrittura<br/> | Valore dell'ID di classe alternativo corrente.<br/>                                                                                                                        |
| [**Apdu**](iscardcmd-get-apdu.md)<br/>                         | Lettura/Scrittura<br/> | Unità [*di dati del protocollo applicativo*](../secgloss/a-gly.md) (APDU, Application Protocol Data Unit) non elaborata.<br/> |
| [**ApduLength**](iscardcmd-get-apdulength.md)<br/>             | Sola lettura<br/>  | Lunghezza dell'APDU.<br/>                                                                                                                                      |
| [**ApduReply**](iscardcmd-get-apdureply.md)<br/>               | Lettura/Scrittura<br/> | [*APDU di risposta.*](../secgloss/r-gly.md)<br/>                                                                        |
| [**ApduReplyLength**](iscardcmd-get-apdureplylength.md)<br/>   | Lettura/Scrittura<br/> | Lunghezza dell'APDU di risposta.<br/>                                                                                                                                |
| [**Classid**](iscardcmd-get-classid.md)<br/>                   | Lettura/Scrittura<br/> | ID di classe dell'APDU.<br/>                                                                                                                                    |
| [**Dati**](iscardcmd-get-data.md)<br/>                         | Sola lettura<br/>  | Campo dati dell'APDU.<br/>                                                                                                                                  |
| [**Id istruzione**](iscardcmd-get-instructionid.md)<br/>       | Lettura/Scrittura<br/> | Byte ID istruzione dall'APDU.<br/>                                                                                                                       |
| [**LeField**](iscardcmd-get-lefield.md)<br/>                   | Sola lettura<br/>  | Campo Le dell'APDU.<br/>                                                                                                                                    |
| [**Nad**](iscardcmd-put-nad.md)<br/>                           | Lettura/Scrittura<br/> | Indirizzo del nodo.<br/>                                                                                                                                            |
| [**P1**](iscardcmd-get-p1.md)<br/>                             | Lettura/Scrittura<br/> | Primo byte del parametro dell'APDU.<br/>                                                                                                                        |
| [**P2**](iscardcmd-get-p2.md)<br/>                             | Lettura/Scrittura<br/> | Secondo byte del parametro dell'APDU.<br/>                                                                                                                       |
| [**P3**](iscardcmd-get-p3.md)<br/>                             | Sola lettura<br/>  | Terzo byte del parametro dell'APDU.<br/>                                                                                                                        |
| [**ReplyNad**](iscardcmd-get-replynad.md)<br/>                 | Lettura/Scrittura<br/> | Indirizzo del nodo usato dalla scheda nel messaggio di risposta.<br/>                                                                                                      |
| [**Stato di risposta**](iscardcmd-get-replystatus.md)<br/>           | Lettura/Scrittura<br/> | [*Parola di stato del messaggio APDU*](../secgloss/r-gly.md) di risposta.<br/>                                                    |
| [**ReplyStatusSW1**](iscardcmd-get-replystatussw1.md)<br/>     | Sola lettura<br/>  | Byte di stato SW1 del messaggio APDU di risposta.<br/>                                                                                                                    |
| [**ReplyStatusSW2**](iscardcmd-get-replystatussw2.md)<br/>     | Sola lettura<br/>  | Byte di stato SW2 del messaggio dell'APDU di risposta.<br/>                                                                                                                    |
| **Tipo**<br/>                                                   | Sola lettura<br/>  | Riservato per utilizzi futuri.<br/>                                                                                                                                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardCmd è definito come \_ D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



 

 
