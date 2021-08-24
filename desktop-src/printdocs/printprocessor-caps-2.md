---
description: Rappresenta le informazioni sulle funzionalità della stampante.
ms.assetid: 70120739-a4e0-4b87-ac7a-40a42fb509ee
title: PRINTPROCESSOR_CAPS_2 struttura (Winspool.h)
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
ms.openlocfilehash: 3425f9477b153721980e3bb44b919b0baea37aa645caea6a3ee328a9ff923eb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824732"
---
# <a name="printprocessor_caps_2-structure"></a>Struttura PRINTPROCESSOR \_ CAPS \_ 2

Rappresenta le informazioni sulle funzionalità della stampante.

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

Valore che indica il numero di versione della struttura .

</dd> <dt>

**dwNupOptions**
</dt> <dd>

Maschera di bit che rappresenta i vari numeri di pagine del documento che la stampante può stampare su un singolo lato di un foglio fisico. Il bit meno significativo rappresenta una pagina del documento per lato, il bit successivo rappresenta 2 pagine di documento per lato e così via. Ad esempio, 0x0000810B la stampante supporta 1, 2, 4, 9 e 16 pagine di documento per lato fisico.

</dd> <dt>

**dwPageOrderFlags**
</dt> <dd>

Valore del flag che indica l'ordine in cui verranno stampate le pagine. Può essere **NORMAL \_ PRINT,** **REVERSE \_ PRINT** o **BOOKLET \_ PRINT.**

</dd> <dt>

**dwNumberOfCopies**
</dt> <dd>

Numero massimo di copie che la stampante può gestire.

</dd> <dt>

**dwNupDirectionCaps**
</dt> <dd>

I modelli disponibili quando più pagine del documento vengono stampate sullo stesso lato di un foglio di carta. I possibili flag sono i seguenti:



| Valore                     | Significato                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------|
| PPCAPS \_ SUBITO \_ IN \_ BASSO | Le pagine vengono visualizzate in righe da destra a sinistra, ogni riga successiva sotto il predecessore.                 |
| PPCAPS \_ VERSO IL BASSO E QUINDI A \_ \_ DESTRA | Le pagine vengono visualizzate in colonne dall'alto verso il basso, ogni colonna successiva a destra del predecessore. |
| PPCAPS \_ VERSO SINISTRA E QUINDI VERSO IL \_ \_ BASSO  | Le pagine vengono visualizzate in righe da sinistra a destra, ogni riga successiva sotto il predecessore.                 |
| PPCAPS \_ VERSO IL BASSO E QUINDI A \_ \_ SINISTRA  | Le pagine vengono visualizzate in colonne dall'alto verso il basso, ogni colonna successiva a sinistra del predecessore.  |



 

</dd> <dt>

**dwNupBorderCaps**
</dt> <dd>

Può essere solo PPCAPS BORDER PRINT, a indicare che, quando vengono stampate più pagine del documento su un singolo lato di un foglio fisico, alla stampante può essere indicato se stampare o meno un bordo intorno all'area stampabile di ogni pagina \_ \_ del documento.

</dd> <dt>

**dwBookletHandlingCaps**
</dt> <dd>

Può essere solo PPCAPS BOOKLET EDGE, a indicare che la \_ stampante può stampare lo stile del \_ libretto.

</dd> <dt>**dwDuplexHandlingCaps**</dt> <dd> 

| Valore                                         | Significato                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PAGINE INVERSA PPCAPS \_ \_ PER IL \_ \_ \_ DUPLEX INVERSO  | Quando si stampa in ordine inverso e duplex, il processore può stampare scambiando l'ordine di ogni coppia di pagine, quindi anziché stampare nell'ordine 4,3,2,1, verranno stampati nell'ordine 3,4,1,2.                                                                                                       |
| PPCAPS \_ NON INVIA PAGINE AGGIUNTIVE PER \_ \_ \_ \_ \_ DUPLEX | Quando si esegue il duplexing, al processore di stampa può essere detto di non inviare una pagina aggiuntiva quando è presente un numero dispari di pagine del documento. Il processore rispetta al meglio il valore possibile, ma nei casi in cui impedire una pagina vuota aggiuntiva causerebbe un output non corretto, le pagine aggiuntive potrebbero comunque essere inviate. |



 

</dd> <dt>

**dwScalingCaps**
</dt> <dd>

Può essere solo PPCAPS SQUARE SCALING, a indicare che \_ la stampante può \_ ridimensionare l'immagine della pagina.

</dd> </dl>

## <a name="remarks"></a>Commenti

I valori per tutti i membri della struttura vengono forniti dalla **funzione GetPrintProcessorCapabilities** documentata in Windows Driver Kit.

Quando un'applicazione chiama [**GetPrinterData,**](getprinterdata.md)lo spooler chiama la funzione **GetPrintProcessorCapabilities** di un processore di stampa e specifica un nome di valore con un formato di _tipo_ di dati **PrintProcCaps \_**, dove *tipo* di dati è il nome di un tipo di dati di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> </dl>

 

 




