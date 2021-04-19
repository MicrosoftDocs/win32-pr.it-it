---
description: La \_ struttura Printer Info \_ 7 specifica le informazioni sulla stampante dei servizi directory.
ms.assetid: 9443855e-df7d-41a1-a0df-5649a97b2915
title: Struttura PRINTER_INFO_7 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_7
- _PRINTER_INFO_7A
- _PRINTER_INFO_7W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3dfa92ead4a1f7dab4f0610145e1e1dee7d04065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318027"
---
# <a name="printer_info_7-structure"></a>\_Struttura info stampa \_ 7

La struttura **Printer \_ info \_ 7** specifica le informazioni sulla stampante dei servizi directory. Usare questa struttura con la funzione [**Seprinter**](setprinter.md) per pubblicare i dati di una stampante nel servizio directory (DS) o per aggiornare o rimuovere i dati pubblicati di una stampante dal DS. Usare questa struttura con la funzione [**GetPrinter**](getprinter.md) per determinare se una stampante è pubblicata nei servizi di dominio Active Directory.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PRINTER_INFO_7 {
  LPTSTR pszObjectGUID;
  DWORD  dwAction;
} PRINTER_INFO_7, *PPRINTER_INFO_7;
```



## <a name="members"></a>Members

<dl> <dt>

**pszObjectGUID**
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene il GUID dell'oggetto coda di stampa del servizio directory associato a una stampante pubblicata. Usare la funzione [**GetPrinter**](getprinter.md) per recuperare questo GUID.

Prima di chiamare il [**Seprinter**](setprinter.md), impostare **pszObjectGUID** su **null**.

</dd> <dt>

**dwAction**
</dt> <dd>

Indica l'azione da eseguire per la funzione [**Seprinter**](setprinter.md) . Per la funzione [**GetPrinter**](getprinter.md) , questo membro indica se la stampante specificata è pubblicata. Questo membro può essere una combinazione dei valori seguenti.



| Valore                                                                                                                                                                                                                                     | Significato                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DSPRINT_PENDING"></span><span id="dsprint_pending"></span><dl> <dt>**DSPRINT \_ 0x80000000 in sospeso**</dt> <dt></dt> </dl>       | [**GetPrinter**](getprinter.md): indica che il sistema sta tentando di completare un'operazione di pubblicazione o di pubblicazione non pubblicata avviata da una chiamata di [**seprinter**](setprinter.md) .<br/> [**Seprinter**](setprinter.md): questo valore non è valido. <br/>                                                |
| <span id="DSPRINT_PUBLISH"></span><span id="dsprint_publish"></span><dl> <dt>**DSPRINT \_ PUBBLICA**</dt> <dt>0x00000001</dt> </dl>       | [**Seprinter**](setprinter.md): pubblica i dati della stampante in DS.<br/> [**GetPrinter**](getprinter.md): indica che la stampante è pubblicata. <br/>                                                                                                                                      |
| <span id="DSPRINT_REPUBLISH"></span><span id="dsprint_republish"></span><dl> <dt>**DSPRINT \_ Ripubblicare**</dt> <dt>0x00000008</dt> </dl> | [**Seprinter**](setprinter.md): i dati DS per la stampante non sono pubblicati e quindi pubblicati nuovamente, aggiornando tutte le proprietà nella stampante pubblicata. La ripubblicazione modifica anche il GUID della stampante pubblicata.<br/> [**GetPrinter**](getprinter.md): non restituisce mai questo valore. <br/> |
| <span id="DSPRINT_UNPUBLISH"></span><span id="dsprint_unpublish"></span><dl> <dt>**DSPRINT \_ Annulla pubblicazione**</dt> <dt>0x00000004</dt> </dl> | [**Seprinter**](setprinter.md): rimuove i dati pubblicati dalla stampante dal DS.<br/> [**GetPrinter**](getprinter.md): indica che la stampante non è pubblicata. <br/>                                                                                                                        |
| <span id="DSPRINT_UPDATE"></span><span id="dsprint_update"></span><dl> <dt>**DSPRINT \_ AGGIORNARE**</dt> <dt>0x00000002</dt> </dl>          | [**Seprinter**](setprinter.md): Aggiorna i dati pubblicati della stampante in DS.<br/> [**GetPrinter**](getprinter.md): non restituisce mai questo valore. <br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura delle **informazioni di stampa \_ \_ 7** viene utilizzata in una chiamata del [**seprinter**](setprinter.md) per pubblicare le informazioni sulla stampante nel servizio directory. I dati pubblicati includono tutti i valori e i dati per la stampante specificata, disponibile nella \_ chiave dello spooler SPLDS, nella chiave del \_ \_ driver SPLDS o nelle \_ \_ \_ chiavi chiave utente SPLDS create da [**SetPrinterDataEx**](setprinterdataex.md).

Per [**Seprinter**](setprinter.md), *pszObjectGUID* deve essere impostato su **null**. Per [**GetPrinter**](getprinter.md), *PSZOBJECTGUID* restituisce il GUID dell'oggetto coda di stampa dei servizi directory associato a una stampante pubblicata. È possibile utilizzare questo GUID con i metodi Active Directory Services Interface (ADSI) per recuperare i dati pubblicati per la stampante. Tuttavia, il metodo consigliato per il recupero dei dati pubblicati consiste nel chiamare la funzione [**GetPrinterDataEx**](getprinterdataex.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ Informazioni sulle stampanti \_ \_ 7W** (Unicode) e **\_ \_ Info stampante \_ 7a** (ANSI)<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




