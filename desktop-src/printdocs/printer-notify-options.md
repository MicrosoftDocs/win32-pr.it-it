---
description: La struttura PRINTER NOTIFY OPTIONS specifica le opzioni per un oggetto di notifica delle modifiche \_ \_ che monitora una stampante o un server di stampa.
ms.assetid: 712c546d-dbb3-4f78-b14e-fbb8619b57f9
title: PRINTER_NOTIFY_OPTIONS struttura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 57b95717e7873f0b73b66d450849d92a2c2ed7053d6d387286cc58144c772ba8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731133"
---
# <a name="printer_notify_options-structure"></a>Struttura PRINTER \_ NOTIFY \_ OPTIONS

La **struttura PRINTER NOTIFY \_ \_ OPTIONS** specifica le opzioni per un oggetto di notifica delle modifiche che monitora una stampante o un server di stampa.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS {
  DWORD                        Version;
  DWORD                        Flags;
  DWORD                        Count;
  PPRINTER_NOTIFY_OPTIONS_TYPE pTypes;
} PRINTER_NOTIFY_OPTIONS, *PPRINTER_NOTIFY_OPTIONS;
```



## <a name="members"></a>Members

<dl> <dt>

**Version**
</dt> <dd>

Versione di questa struttura. Impostare questo membro su 2.

</dd> <dt>

**Flag**
</dt> <dd>

Flag di bit. Se si imposta il flag PRINTER NOTIFY OPTIONS REFRESH in una chiamata alla funzione \_ \_ \_ [**FindNextPrinterChangeNotification,**](findnextprinterchangenotification.md) la funzione fornisce i dati correnti per tutti i campi di informazioni sulla stampante monitorati. La [**funzione FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) ignora il **membro Flags.**

</dd> <dt>

**Count**
</dt> <dd>

Numero di elementi nella matrice **pTypes.**

</dd> <dt>

**pTypes**
</dt> <dd>

Puntatore a una matrice di [**strutture PRINTER NOTIFY OPTIONS \_ \_ \_ TYPE.**](printer-notify-options-type.md) Usare un elemento di questa matrice per specificare i campi di informazioni sulla stampante da monitorare e un elemento per specificare i campi di informazioni sul processo da monitorare. È possibile monitorare le informazioni sulla stampante, le informazioni sul processo o entrambe.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare questa struttura con la [**funzione FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) per specificare il set di campi relativi alle informazioni sulla stampante o sul processo da monitorare per la modifica.

Usare questa struttura con la [**funzione FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) per richiedere i dati correnti per tutti i campi di informazioni sulla stampante e sul processo monitorati. In questo caso, il **membro Flags** specifica il flag PRINTER \_ NOTIFY OPTIONS REFRESH e la funzione ignora gli altri membri \_ della \_ struttura.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**TIPO DI \_ OPZIONI DI \_ NOTIFICA \_ STAMPANTE**](printer-notify-options-type.md)
</dt> </dl>

 

 




