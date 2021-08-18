---
description: In MOF i numeri sono cifre che descrivono valori numerici. MOF offre un'ampia gamma di tipi di dati che si traducono in Automazione e consente anche che tali numeri siano in formati diversi. Nella tabella seguente sono elencati i valori numerici supportati da MOF.
ms.assetid: 7a18ed36-9c12-42be-a4ee-0f6c0097b130
ms.tgt_platform: multiple
title: Numeri (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f3441988bb91d4bb2f3742016f01cb69996e3dcb55081a6723d851ed74cc1cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555141"
---
# <a name="numbers-wmi"></a>Numeri (WMI)

In MOF i numeri sono cifre che descrivono valori numerici. MOF offre un'ampia gamma di tipi di dati che si traducono in Automazione e consente anche che tali numeri siano in formati diversi. Nella tabella seguente sono elencati i valori numerici supportati da MOF.



| Tipo di dati  | Tipo di automazione | Descrizione                                                                                                                                                             |
|------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **sint8**  | **VT \_ I2**      | Intero con segno a 8 bit.<br/>                                                                                                                                        |
| **sint16** | **VT \_ I2**      | Intero con segno a 16 bit.<br/>                                                                                                                                       |
| **sint32** | VT \_ I4          | Intero con segno a 32 bit.<br/>                                                                                                                                       |
| **sint64** | **VT \_ BSTR**    | Intero con segno a 64 bit in formato stringa. Questo tipo segue il formato esadecimale o decimale in base alle regole American National Standards Institute (ANSI) C.<br/> |
| **real32** | **VT \_ R4**      | Valore a virgola mobile a 4 byte che segue lo standard IEEE (Institute of Electrical and Electronics Engineers, Inc.<br/>                                        |
| **real64** | **VT \_ R8**      | Valore a virgola mobile a 8 byte che segue lo standard IEEE.<br/>                                                                                                  |
| **uint8**  | **VT \_ UI1**     | Intero senza segno a 8 bit.<br/>                                                                                                                                      |
| **uint16** | **VT \_ I4**      | Intero senza segno a 16 bit.<br/>                                                                                                                                     |
| **uint32** | **VT \_ I4**      | Intero senza segno a 32 bit.<br/>                                                                                                                                     |
| **uint64** | **VT \_ BSTR**    | Intero senza segno a 64 bit in formato stringa. Questo tipo segue il formato esadecimale o decimale in base alle regole ANSI C.<br/>                                           |



 

Anche se flessibile, il codice MOF riscontra alcune modifiche quando si lavora con Automazione:

-   È necessario codificare interi a 64 bit come stringhe.

    Automazione non supporta un tipo integrale a 64 bit.

-   I tipi di automazione non sempre corrispondono in bit ai tipi di dati MOF.

    Automazione, ad esempio, usa VT \_ I4 per restituire un valore senza segno a 16 bit. Questa discrepanza esiste a causa di problemi di estensione del segno. Se Automazione usasse VT I2 anziché \_ VT \_ I4, 65.536 apparirebbe come valore 1, causando problemi di tipo e intervallo. Analogamente, Automazione rappresenta il **tipo uint32** come VT I4 perché non esiste alcun tipo Integer più grande per \_ **contenere uint32**.

-   Non è necessario modificare alcuna rappresentazione per i tipi numerici a 8 bit.

    Automazione supporta VT \_ UI1, un tipo senza segno a 8 bit.

MOF supporta costanti long. Si dichiara una costante long usando una semplice serie di cifre con un segno negativo facoltativo. Una costante long non può superare le dimensioni della variabile dichiarata per contenerla. Alcuni esempi di costanti long sono 1000 e 12310.

MOF supporta anche formati numerici alternativi. Nella tabella seguente sono elencati i caratteri speciali che è necessario usare per descrivere le costanti esadecimali, binarie e ottali.



| Costante               | Carattere speciale     | Esempio                   |
|------------------------|-----------------------|---------------------------|
| Decimal<br/>     | Nessuno<br/>       | val = 65<br/>       |
| Valore esadecimale<br/> | Prefisso 0x<br/>  | val = 0x41<br/>     |
| Ottale<br/>       | 0 iniziale<br/>  | val = 0101<br/>     |
| Binary<br/>      | Finale B<br/> | val = 1000001B<br/> |



 

È possibile usare una costante a virgola mobile per rappresentare la notazione scientifica e le frazioni, come illustrato di seguito:

``` syntax
3.14
-3.14
-1.2778E+02
```

WMI considera le costanti a virgola mobile come **tipi \_ VT R8** per Automazione.

Nell'esempio seguente vengono descritte le dichiarazioni di classe e istanza che illustrano come usare ognuno dei tipi di dati numerici per impostare le proprietà:

``` syntax
Class NumericDataClass
 {
   [key] uint8 Duint8;
   SInt8       Dchar;
   UInt16      Dtword;
   Sint16      Dinst16;
   UInt32      Ddword;
   Sint32      Dinst1;
   Sint32      Dinst2;
   Sint32      Dinst3;
   Sint32      Dinst4;
   Sint32      Dinst5;
   Real32      Dfloat;
   Real64      Ddouble1;
   Real64      Ddouble2;
 };

instance of NumericDataClass
 {
   Duint8   =  122;
   Dchar    = -128;
   Dtword   =  30;
   Dinst16  = -1445;
   Ddword   =  6987777;
   Dinst1   = -455589;
   Dinst2   =  23;
   Dinst3   =  03;         // Base 8
   Dinst4   =  0xFe;       // Base 16
   Dinst5   =  11b;        // Base 2
   Dfloat   =  3.1478;
   Ddouble1 =  99987.3654;
   Ddouble2 =  2.3e-2;
 };
```

 

 




