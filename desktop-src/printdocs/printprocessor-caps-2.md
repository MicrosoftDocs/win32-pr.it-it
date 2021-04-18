---
description: Rappresenta le informazioni sulla funzionalità della stampante.
ms.assetid: 70120739-a4e0-4b87-ac7a-40a42fb509ee
title: Struttura PRINTPROCESSOR_CAPS_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_2
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1847ffa1912a8638476ce80dfbdb71c40fc376d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315981"
---
# <a name="printprocessor_caps_2-structure"></a>\_Struttura PRINTPROCESSOR Caps \_ 2

Rappresenta le informazioni sulla funzionalità della stampante.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PRINTPROCESSOR_CAPS_2 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
  DWORD dwNupDirectionCaps;
  DWORD dwNupBorderCaps;
  DWORD dwBookletHandlingCaps;
  DWORD dwDuplexHandlingCaps;
  DWORD dwScalingCaps;
} PRINTPROCESSOR_CAPS_2, *PPRINTPROCESSOR_CAPS_2;
```



## <a name="members"></a>Members

<dl> <dt>

**dwLevel**
</dt> <dd>

Valore che indica il numero di versione della struttura.

</dd> <dt>

**dwNupOptions**
</dt> <dd>

Maschera di bit che rappresenta i vari numeri di pagine del documento che la stampante è in grado di stampare su un solo lato di un foglio fisico. Il bit meno significativo rappresenta una pagina del documento per lato, il bit successivo rappresenta 2 pagine del documento per lato e così via. Ad esempio, 0x0000810B indica che la stampante supporta 1, 2, 4, 9 e 16 pagine documento per lato fisico.

</dd> <dt>

**dwPageOrderFlags**
</dt> <dd>

Valore del flag che indica l'ordine in cui verranno stampate le pagine. Può essere stampa **normale \_**, **\_ Stampa inversa** o **opuscolo \_**.

</dd> <dt>

**dwNumberOfCopies**
</dt> <dd>

Numero massimo di copie che la stampante è in grado di gestire.

</dd> <dt>

**dwNupDirectionCaps**
</dt> <dd>

Modelli disponibili quando più pagine del documento vengono stampate sullo stesso lato di un foglio di carta. I flag possibili sono i seguenti:



| Valore                     | Significato                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------|
| PPCAPS \_ subito \_ dopo \_ | Le pagine vengono visualizzate in righe da destra a sinistra, ogni riga successiva al di sotto del suo predecessore.                 |
| PPCAPS \_ giù \_ a \_ destra | Le pagine vengono visualizzate in colonne dall'alto verso il basso, ciascuna colonna successiva a destra del relativo predecessore. |
| PPCAPS verso il \_ \_ \_ basso  | Le pagine vengono visualizzate in righe da sinistra a destra, ogni riga successiva al di sotto del suo predecessore.                 |
| PPCAPS \_ a \_ \_ sinistra  | Le pagine vengono visualizzate in colonne dall'alto verso il basso, ogni colonna successiva a sinistra del relativo predecessore.  |



 

</dd> <dt>

**dwNupBorderCaps**
</dt> <dd>

Può essere solo \_ Stampa bordo PPCAPS \_ , a indicare che, quando vengono stampate più pagine del documento su un solo lato di un foglio fisico, è possibile indicare alla stampante se stampare un bordo intorno all'area stampabile di ogni pagina del documento.

</dd> <dt>

**dwBookletHandlingCaps**
</dt> <dd>

Può essere PPCAPS solo \_ per \_ il bordo dell'opuscolo, a indicare che la stampante può stampare lo stile del libretto.

</dd> <dt>**dwDuplexHandlingCaps**</dt> <dd> 

| Valore                                         | Significato                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PPCAPS \_ le \_ pagine inverse \_ per \_ duplex invertito \_  | Quando si esegue la stampa in ordine inverso e duplexing, il processore può stampare lo swap dell'ordine di ogni coppia di pagine, quindi anziché stampare nell'ordine 4, 3, 2, 1, verranno stampate nell'ordine 3, 4, 1, 2.                                                                                                       |
| PPCAPS \_ non \_ inviano \_ \_ pagine aggiuntive \_ per \_ duplex | Quando si esegue la duplexing, il processore di stampa può essere avvisato di non inviare una pagina aggiuntiva quando è presente un numero dispari di pagine documento. Il processore rispetterà il valore nel modo migliore possibile, ma nei casi in cui impedire una pagina vuota aggiuntiva potrebbe causare un output non corretto, le pagine aggiuntive potrebbero essere ancora inviate. |



 

</dd> <dt>

**dwScalingCaps**
</dt> <dd>

Può essere PPCAPS solo \_ il \_ ridimensionamento quadrato, a indicare che la stampante può ridimensionare l'immagine della pagina.

</dd> </dl>

## <a name="remarks"></a>Commenti

I valori per tutti i membri della struttura sono forniti dalla funzione **GetPrintProcessorCapabilities** , documentata in Windows Driver Kit.

Quando un'applicazione chiama [**GetPrinterData**](getprinterdata.md), lo spooler chiama la funzione **GetPrintProcessorCapabilities** di un processore di stampa e specifica un nome di valore con formato **PrintProcCaps \_**_DataType_, dove *DataType* è il nome di un tipo di dati di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> </dl>

 

 




