---
description: In MOF i numeri sono cifre che descrivono valori numerici. MOF fornisce un'ampia gamma di tipi di dati che si traducono in automazione e consente inoltre che tali numeri siano in formati diversi. Nella tabella seguente sono elencati i valori numerici supportati da MOF.
ms.assetid: 7a18ed36-9c12-42be-a4ee-0f6c0097b130
ms.tgt_platform: multiple
title: Numeri (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad348820e0294e76ba059a06b6daa6f1c916d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305575"
---
# <a name="numbers-wmi"></a>Numeri (WMI)

In MOF i numeri sono cifre che descrivono valori numerici. MOF fornisce un'ampia gamma di tipi di dati che si traducono in automazione e consente inoltre che tali numeri siano in formati diversi. Nella tabella seguente sono elencati i valori numerici supportati da MOF.



| Tipo di dati  | Tipo di automazione | Descrizione                                                                                                                                                             |
|------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **sint8**  | **\_I2 VT**      | Signed Integer a 8 bit.<br/>                                                                                                                                        |
| **sint16** | **\_I2 VT**      | Intero con segno a 16 bit.<br/>                                                                                                                                       |
| **sint32** | VT \_ I4          | Signed Integer a 32 bit.<br/>                                                                                                                                       |
| **sint64** | **\_BSTR VT**    | Signed Integer a 64 bit in formato stringa. Questo tipo segue il formato esadecimale o decimale in base alle regole del American National Standards Institute (ANSI) C.<br/> |
| **real32** | **\_R4 VT**      | valore a virgola mobile a 4 byte che segue lo standard IEEE (Institute of Electrical and Electronics Engineers, Inc.).<br/>                                        |
| **real64** | **VT \_ R8**      | valore a virgola mobile a 8 byte che segue lo standard IEEE.<br/>                                                                                                  |
| **Uint8**  | **\_Ui1 VT**     | Intero senza segno a 8 bit.<br/>                                                                                                                                      |
| **UInt16** | **VT \_ I4**      | Intero senza segno a 16 bit.<br/>                                                                                                                                     |
| **uint32** | **VT \_ I4**      | Intero senza segno a 32 bit.<br/>                                                                                                                                     |
| **uint64** | **\_BSTR VT**    | Intero senza segno a 64 bit in formato stringa. Questo tipo segue il formato esadecimale o decimale secondo le regole ANSI C.<br/>                                           |



 

Sebbene il codice MOF flessibile riscontri alcune modifiche durante l'automazione:

-   È necessario codificare interi a 64 bit come stringhe.

    L'automazione non supporta un tipo integrale a 64 bit.

-   I tipi di automazione non sempre corrispondono alle dimensioni dei bit per i tipi di dati MOF.

    Ad esempio, l'automazione USA VT \_ I4 per restituire un valore a 16 bit senza segno. Questa discrepanza esiste a causa di problemi di estensione della firma. Se l'automazione usava VT \_ I2 anziché VT \_ I4, 65.536 sembrerebbe il valore 1, causando problemi di tipo e di intervallo. Analogamente, l'automazione rappresenta il tipo **UInt32** come VT \_ I4 perché non esiste alcun tipo integer più grande che contenga **UInt32**.

-   Non è necessario modificare alcuna rappresentazione per i tipi numerici a 8 bit.

    L'automazione supporta VT \_ Ui1, un tipo senza segno a 8 bit.

MOF supporta costanti lunghe. Viene dichiarata una costante lungo usando una semplice serie di cifre con un segno negativo facoltativo. Una costante Long non può superare le dimensioni della variabile dichiarata in modo da contenerla. Alcuni esempi di costanti lunghe sono 1000 e 12310.

MOF supporta inoltre formati numerici alternativi. Nella tabella seguente sono elencati i caratteri speciali che è necessario utilizzare per descrivere le costanti esadecimali, binarie e ottali.



| Costante               | Carattere speciale     | Esempio                   |
|------------------------|-----------------------|---------------------------|
| Decimal<br/>     | nessuno<br/>       | Val = 65<br/>       |
| Valore esadecimale<br/> | prefisso 0x<br/>  | Val = 0x41<br/>     |
| Ottale<br/>       | 0 iniziali<br/>  | Val = 0101<br/>     |
| Binary<br/>      | Finali B<br/> | Val = 1000001B<br/> |



 

È possibile usare una costante a virgola mobile per rappresentare la notazione scientifica e le frazioni, come illustrato di seguito:

``` syntax
3.14
-3.14
-1.2778E+02
```

WMI considera le costanti a virgola mobile come tipi di **VT \_ R8** per l'automazione.

Nell'esempio seguente vengono descritte le dichiarazioni di classe e istanza che illustrano come utilizzare ciascuno dei tipi di dati numerici per impostare le proprietà:

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

 

 




