---
description: Fornisce i metodi necessari per creare e gestire un'unità dati del protocollo dell'applicazione (APDU) per smart card.
ms.assetid: fd84bb2e-27da-4670-b8e8-56c7948b78bb
title: Interfaccia ISCardCmd (Scarddat. h)
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
ms.openlocfilehash: f14291f3777dcdc8b661f96f94d987209100a365
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049364"
---
# <a name="iscardcmd-interface"></a>Interfaccia ISCardCmd

\[L'interfaccia **ISCardCmd** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

L'interfaccia **ISCardCmd** fornisce i metodi necessari per creare e gestire un' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) [*Smart Card*](../secgloss/s-gly.md) (APDU). Questa interfaccia incapsula due buffer:

-   Il buffer APDU contiene la sequenza di comandi che verrà inviata alla scheda.
-   Il buffer APDUReply contiene i dati restituiti dalla scheda dopo l'esecuzione del comando APDU. questi dati sono anche detti APDU restituiti.

Nell'esempio seguente viene illustrato un utilizzo tipico dell'interfaccia **ISCardCmd** . L'interfaccia **ISCardCmd** viene utilizzata per creare un APDU.

**Per inviare una transazione a una scheda specifica**

1.  Creare un'interfaccia di [**scheda**](iscard.md) e connettersi a una smart card.
2.  Creare un'interfaccia **ISCardCmd** .
3.  Compilare un comando APDU della smart card usando l'interfaccia [**ISCardISO7816**](iscardiso7816.md) o uno dei metodi di compilazione **ISCardCmd** .
4.  Eseguire il comando nella smart card chiamando il metodo di interfaccia di [**scheda**](iscard.md) appropriato.
5.  Valutare la risposta restituita.
6.  Ripetere la procedura in base alle esigenze.
7.  Rilasciare l'interfaccia **ISCardCmd** e altre in base alle esigenze.

## <a name="members"></a>Membri

L'interfaccia **ISCardCmd** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardCmd** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **ISCardCmd** dispone di questi metodi.



| Metodo                                       | Descrizione                                                                                                |
|:---------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**BuildCmd**](iscardcmd-buildcmd.md)       | Costruisce un APDU del comando valido per la trasmissione a una smart card.<br/>                               |
| [**Deselezionare**](iscardcmd-clear.md)             | Cancella i buffer dei messaggi APDU e APDU di risposta.<br/>                                             |
| [**Incapsulare**](iscardcmd-encapsulate.md) | Incapsula il comando specificato APDU in un altro comando APDU per la trasmissione a una smart card.<br/> |



 

### <a name="properties"></a>Proprietà

L'interfaccia **ISCardCmd** ha queste proprietà.



| Proprietà                                                              | Tipo di accesso           | Descrizione                                                                                                                                                         |
|:----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AlternateClassId**](iscardcmd-get-alternateclassid.md)<br/> | Lettura/Scrittura<br/> | Valore corrente dell'ID di classe alternativa.<br/>                                                                                                                        |
| [**APDU**](iscardcmd-get-apdu.md)<br/>                         | Lettura/Scrittura<br/> | [*Unità dati del protocollo applicazione*](../secgloss/a-gly.md) (APDU) non elaborata.<br/> |
| [**ApduLength**](iscardcmd-get-apdulength.md)<br/>             | Sola lettura<br/>  | Lunghezza di APDU.<br/>                                                                                                                                      |
| [**ApduReply**](iscardcmd-get-apdureply.md)<br/>               | Lettura/Scrittura<br/> | [*APDU di risposta*](../secgloss/r-gly.md).<br/>                                                                        |
| [**ApduReplyLength**](iscardcmd-get-apdureplylength.md)<br/>   | Lettura/Scrittura<br/> | Lunghezza del APDU di risposta.<br/>                                                                                                                                |
| [**ClassId**](iscardcmd-get-classid.md)<br/>                   | Lettura/Scrittura<br/> | ID classe del APDU.<br/>                                                                                                                                    |
| [**Data**](iscardcmd-get-data.md)<br/>                         | Sola lettura<br/>  | Campo dati di APDU.<br/>                                                                                                                                  |
| [**InstructionId**](iscardcmd-get-instructionid.md)<br/>       | Lettura/Scrittura<br/> | ID istruzione byte da APDU.<br/>                                                                                                                       |
| [**LeField**](iscardcmd-get-lefield.md)<br/>                   | Sola lettura<br/>  | Campo le di APDU.<br/>                                                                                                                                    |
| [**Nad**](iscardcmd-put-nad.md)<br/>                           | Lettura/Scrittura<br/> | Indirizzo del nodo.<br/>                                                                                                                                            |
| [**P1**](iscardcmd-get-p1.md)<br/>                             | Lettura/Scrittura<br/> | Primo parametro byte di APDU.<br/>                                                                                                                        |
| [**P2**](iscardcmd-get-p2.md)<br/>                             | Lettura/Scrittura<br/> | Secondo parametro byte di APDU.<br/>                                                                                                                       |
| [**P3**](iscardcmd-get-p3.md)<br/>                             | Sola lettura<br/>  | Terzo parametro byte di APDU.<br/>                                                                                                                        |
| [**ReplyNad**](iscardcmd-get-replynad.md)<br/>                 | Lettura/Scrittura<br/> | Indirizzo del nodo utilizzato dalla scheda nel messaggio di risposta.<br/>                                                                                                      |
| [**ReplyStatus**](iscardcmd-get-replystatus.md)<br/>           | Lettura/Scrittura<br/> | Parola di stato del messaggio di [*risposta APDU*](../secgloss/r-gly.md) .<br/>                                                    |
| [**ReplyStatusSW1**](iscardcmd-get-replystatussw1.md)<br/>     | Sola lettura<br/>  | Messaggio di stato SW1 del messaggio di risposta APDU.<br/>                                                                                                                    |
| [**ReplyStatusSW2**](iscardcmd-get-replystatussw2.md)<br/>     | Sola lettura<br/>  | Risposta APDU messaggio SW2 stato byte.<br/>                                                                                                                    |
| **Tipo**<br/>                                                   | Sola lettura<br/>  | Riservato per utilizzi futuri.<br/>                                                                                                                                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



 

 
