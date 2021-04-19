---
description: La stampante \_ info \_ 6 specifica il valore dello stato di una stampante.
ms.assetid: f26fe75b-7c97-47ad-892f-d9e40331fa5d
title: Struttura PRINTER_INFO_6 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_6
- _PRINTER_INFO_6A
- _PRINTER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0ee4e86590483ec1751fa088fd56770c5891df0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318032"
---
# <a name="printer_info_6-structure"></a>\_Struttura info stampa \_ 6

La **stampante \_ info \_ 6** specifica il valore dello stato di una stampante.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PRINTER_INFO_6 {
  DWORD dwStatus;
} PRINTER_INFO_6, *PPRINTER_INFO_6;
```



## <a name="members"></a>Members

<dl> <dt>

**dwStatus**
</dt> <dd>

Stato della stampante. Questo membro può essere qualsiasi combinazione ragionevole dei valori seguenti.



| Valore                               | Significato                                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| stato della stampante \_ \_ occupato               | La stampante è occupata.                                                                                          |
| \_sportello dello stato della stampante \_ \_ aperto         | Lo sportello della stampante è aperto.                                                                                     |
| \_errore di stato della stampante \_              | Non usato.                                                                                                     |
| \_inizializzazione dello stato della stampante \_       | È in corso l'inizializzazione della stampante.                                                                                  |
| \_io stato \_ stampante \_ attivo         | La stampante è in uno stato di input/output attivo                                                                |
| \_feed manuale dello stato della stampante \_ \_       | La stampante è in uno stato di avanzamento manuale.                                                                        |
| \_stato stampante \_ senza \_ toner          | La stampante ha esaurito il toner.                                                                                  |
| stato della stampante \_ \_ non \_ disponibile     | La stampante non è disponibile per la stampa.                                                                    |
| stato della stampante \_ \_ offline            | La stampante non è in linea.                                                                                       |
| \_ \_ \_ \_ memoria insufficiente per lo stato della stampante    | Memoria esaurita per la stampante.                                                                            |
| \_Cestino di \_ output stato stampante \_ \_ completo  | Il cassetto di uscita della stampante è pieno.                                                                             |
| pagina di stato della stampante \_ \_ \_ Punt         | La stampante non è in grado di stampare la pagina corrente.                                                                    |
| \_ \_ inceppamento carta stato stampante \_         | La carta è bloccata nella stampante                                                                                |
| \_carta dello stato della stampante in \_ \_ uscita         | La stampante ha esaurito la carta.                                                                                  |
| \_ \_ problema relativo alla carta di stato della stampante \_     | La stampante presenta un problema relativo alla carta.                                                                              |
| stato della stampante \_ \_ sospeso             | La stampante è sospesa.                                                                                        |
| \_stato stampante \_ in attesa di \_ eliminazione  | La stampante è in attesa di eliminazione in seguito a una chiamata alla funzione [**DeletePrinter**](deleteprinter.md) . |
| \_risparmio di stato della stampante \_ \_        | La stampante è in modalità risparmio energia.                                                                            |
| \_stampa dello stato della stampante \_           | Viene stampata la stampante.                                                                                      |
| \_elaborazione dello stato della stampante \_         | La stampante sta elaborando un comando dalla funzione [**Seprinter**](setprinter.md) .                       |
| \_Server stato \_ stampante \_ sconosciuto    | Lo stato della stampante è sconosciuto.                                                                                |
| \_ \_ toner stato stampante \_ basso         | Il toner della stampante è insufficiente.                                                                                  |
| \_ \_ intervento dell'utente sullo stato della stampante \_ | La stampante presenta un errore che richiede all'utente di eseguire un'operazione.                                              |
| stato della stampante \_ \_ in attesa            | La stampante è in attesa.                                                                                       |
| \_stato della \_ stampante \_ attivo        | La stampante è in fase di riscaldamento.                                                                                    |



 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ \_ Info stampante \_ 6W** (Unicode) e **\_ \_ Info stampante \_ 6a** (ANSI)<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**\_Informazioni stampante \_ 1**](printer-info-1.md)
</dt> <dt>

[**\_Informazioni stampante \_ 2**](printer-info-2.md)
</dt> <dt>

[**\_Informazioni stampante \_ 3**](printer-info-3.md)
</dt> <dt>

[**\_Informazioni stampante \_ 4**](printer-info-4.md)
</dt> <dt>

[**\_Informazioni stampante \_ 5**](printer-info-5.md)
</dt> </dl>

 

 




