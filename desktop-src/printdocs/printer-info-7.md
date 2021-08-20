---
description: La struttura PRINTER \_ INFO \_ 7 specifica le informazioni sulla stampante dei servizi directory.
ms.assetid: 9443855e-df7d-41a1-a0df-5649a97b2915
title: PRINTER_INFO_7 struttura (Winspool.h)
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
ms.openlocfilehash: c8ba37176bb970883533be1e0ddcc47a09b164bf48767442f75096828c9bce5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867767"
---
# <a name="printer_info_7-structure"></a>Struttura PRINTER \_ INFO \_ 7

La **struttura PRINTER INFO \_ \_ 7** specifica le informazioni sulla stampante dei servizi directory. Usare questa struttura con la funzione [**SetPrinter**](setprinter.md) per pubblicare i dati di una stampante nel servizio directory o per aggiornare o rimuovere i dati pubblicati di una stampante da DS. Usare questa struttura con la [**funzione GetPrinter**](getprinter.md) per determinare se una stampante viene pubblicata in DS.

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

Puntatore a una stringa con terminazione Null contenente il GUID dell'oggetto coda di stampa del servizio directory associato a una stampante pubblicata. Usare la [**funzione GetPrinter**](getprinter.md) per recuperare questo GUID.

Prima di [**chiamare SetPrinter,**](setprinter.md)impostare **pszObjectGUID** su **NULL.**

</dd> <dt>

**dwAction**
</dt> <dd>

Indica l'azione da eseguire per la funzione [**SetPrinter.**](setprinter.md) Per la [**funzione GetPrinter,**](getprinter.md) questo membro indica se la stampante specificata è pubblicata. Questo membro può essere una combinazione dei valori seguenti.



| Valore                                                                                                                                                                                                                                     | Significato                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DSPRINT_PENDING"></span><span id="dsprint_pending"></span><dl> <dt>**DSPRINT \_ IN SOSPESO**</dt> <dt>0x80000000</dt> </dl>       | [**GetPrinter:**](getprinter.md)indica che il sistema sta tentando di completare un'operazione di pubblicazione o annullamento della pubblicazione avviata da una [**chiamata a SetPrinter.**](setprinter.md)<br/> [**SetPrinter:**](setprinter.md)questo valore non è valido. <br/>                                                |
| <span id="DSPRINT_PUBLISH"></span><span id="dsprint_publish"></span><dl> <dt>**DSPRINT \_ PUBBLICAZIONE**</dt> <dt>0x00000001</dt> </dl>       | [**SetPrinter:**](setprinter.md)pubblica i dati della stampante nel DS.<br/> [**GetPrinter**](getprinter.md): indica che la stampante è pubblicata. <br/>                                                                                                                                      |
| <span id="DSPRINT_REPUBLISH"></span><span id="dsprint_republish"></span><dl> <dt>**DSPRINT \_ RIPUBBLICAre**</dt> <dt>0x00000008</dt> </dl> | [**SetPrinter:**](setprinter.md)i dati DS per la stampante non vengono pubblicati e quindi pubblicati di nuovo, aggiornando tutte le proprietà nella stampante pubblicata. La ri-pubblicazione modifica anche il GUID della stampante pubblicata.<br/> [**GetPrinter:**](getprinter.md)non restituisce mai questo valore. <br/> |
| <span id="DSPRINT_UNPUBLISH"></span><span id="dsprint_unpublish"></span><dl> <dt>**DSPRINT \_ Annullare la pubblicazione**</dt> <dt>0x00000004</dt> </dl> | [**SetPrinter:**](setprinter.md)rimuove i dati pubblicati della stampante dal servizio Di rete.<br/> [**GetPrinter**](getprinter.md): indica che la stampante non è pubblicata. <br/>                                                                                                                        |
| <span id="DSPRINT_UPDATE"></span><span id="dsprint_update"></span><dl> <dt>**DSPRINT \_ AGGIORNAMENTO**</dt> <dt>0x00000002</dt> </dl>          | [**SetPrinter:**](setprinter.md)aggiorna i dati pubblicati della stampante nel DS.<br/> [**GetPrinter:**](getprinter.md)non restituisce mai questo valore. <br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La **struttura PRINTER INFO \_ \_ 7** viene usata in una [**chiamata SetPrinter**](setprinter.md) per pubblicare le informazioni della stampante nel servizio directory. I dati pubblicati includono tutti i valori e i dati per la stampante specificata presenti nelle chiavi SPLDS \_ SPOOLER \_ KEY, SPLDS DRIVER KEY o \_ \_ SPLDS USER KEY create \_ da \_ [**SetPrinterDataEx.**](setprinterdataex.md)

Per [**SetPrinter,**](setprinter.md) *pszObjectGUID* deve essere impostato su **NULL.** Per [**GetPrinter**](getprinter.md), *pszObjectGUID* restituisce il GUID dell'oggetto coda di stampa dei servizi directory associato a una stampante pubblicata. È possibile usare questo GUID con i metodi ADSI (Active Directory Services Interface) per recuperare i dati pubblicati per la stampante. Tuttavia, il metodo consigliato per recuperare i dati pubblicati è chiamare la [**funzione GetPrinterDataEx.**](getprinterdataex.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ PRINTER \_ INFO \_ 7W** (Unicode) e **\_ PRINTER INFO \_ \_ 7A** (ANSI)<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




