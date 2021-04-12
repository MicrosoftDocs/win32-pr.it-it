---
title: Nuovi tipi di dati
description: Sono state introdotte tre classi di tipi di dati per i tipi di dati a precisione fissa di Windows a 64 bit, i tipi di precisione del puntatore e i tipi specifici di precisione del puntatore.
ms.assetid: 016977d4-e7bf-463e-9755-7ef13f16e9e5
keywords:
- Guida per programmatori Windows a 64 bit Guida alla programmazione Windows a 64 bit, tipi di dati
- tipi di dati programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6cf5960b5344da1d459d12dee96a2f67f2cfbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338918"
---
# <a name="the-new-data-types"></a>Nuovi tipi di dati

Sono state introdotte tre classi di tipi di dati per Windows a 64 bit: tipi di dati a precisione fissa, tipi di precisione del puntatore e tipi specifici di precisione del puntatore. Questi tipi sono stati aggiunti all'ambiente di sviluppo per consentire agli sviluppatori di prepararsi per Windows a 64 bit. Questi tipi sono derivati dall'Integer di base in linguaggio C e dai tipi lunghi. È quindi possibile usare questi tipi di dati nel codice compilato e testato in Windows a 32 bit, quindi ricompilarlo con il compilatore a 64 bit quando è destinato a Windows a 64 bit.

Anche per le applicazioni destinate solo a Windows a 32 bit, l'adozione di questi nuovi tipi di dati rende il codice più affidabile. Per usare questi tipi di dati, è necessario analizzare il codice per l'utilizzo del puntatore, il polimorfismo e le definizioni dei dati potenzialmente non sicuri. Ad esempio, quando una variabile è di tipo **ULONG \_ ptr**, è chiaro che verrà usata per il cast dei puntatori per operazioni aritmetiche o polimorfismo. Non è possibile indicare tale utilizzo direttamente utilizzando i tipi di dati meno recenti. È possibile eseguire questa operazione indirettamente usando la denominazione dei tipi derivati o la notazione ungherese, ma entrambe le tecniche sono soggette a errori.

Tutti questi tipi di dati sono dichiarati in BaseTsd. h. Per ulteriori informazioni, incluse le definizioni di questi tipi di dati, vedere [tipi di dati di Windows](/windows/desktop/WinProg/windows-data-types).

## <a name="fixed-precision"></a>Precisione fissa

I tipi di dati a precisione fissa hanno la stessa lunghezza in Windows 32 e 64 bit. Per tenere presente questo aspetto, la relativa precisione fa parte del nome del tipo di dati. Di seguito sono riportati i tipi di dati a precisione fissa.



| Termine                                                                       | Descrizione                        |
|----------------------------------------------------------------------------|------------------------------------|
| <span id="DWORD32"></span><span id="dword32"></span>**DWORD32**<br/> | Intero senza segno a 32 bit<br/> |
| <span id="DWORD64"></span><span id="dword64"></span>**DWORD64**<br/> | Intero senza segno a 64 bit<br/> |
| <span id="INT32"></span><span id="int32"></span>**INT32**<br/>       | Intero con segno a 32 bit<br/>   |
| <span id="INT64"></span><span id="int64"></span>**INT64**<br/>       | Intero con segno a 64 bit<br/>   |
| <span id="LONG32"></span><span id="long32"></span>**LONG32**<br/>    | Intero con segno a 32 bit<br/>   |
| <span id="LONG64"></span><span id="long64"></span>**LONG64**<br/>    | Intero con segno a 64 bit<br/>   |
| <span id="UINT32"></span><span id="uint32"></span>**UINT32**<br/>    | **Int32** senza segno<br/>      |
| <span id="UINT64"></span><span id="uint64"></span>**UINT64**<br/>    | **Int64** senza segno<br/>      |
| <span id="ULONG32"></span><span id="ulong32"></span>**ULONG32**<br/> | Unsigned **LONG32**<br/>     |
| <span id="ULONG64"></span><span id="ulong64"></span>**ULONG64**<br/> | Unsigned **long64**<br/>     |



 

## <a name="pointer-precision"></a>Precisione del puntatore

Quando la precisione del puntatore cambia (ovvero, poiché diventa 32 bit su Windows a 32 bit e 64 bit con Windows a 64 bit), i tipi di dati di precisione del puntatore riflettono la precisione di conseguenza. Pertanto, è possibile eseguire il cast di un puntatore a uno di questi tipi quando si esegue l'aritmetica dei puntatori; Se la precisione del puntatore è 64 bit, il tipo è 64 bit. I tipi di conteggio riflettono anche le dimensioni massime a cui un puntatore può fare riferimento. Di seguito sono riportati i tipi di conteggio e precisione del puntatore.



| Termine                                                                              | Descrizione                                                                                                                      |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span id="DWORD_PTR"></span><span id="dword_ptr"></span>**\_ptr DWORD**<br/> | Tipo long senza segno per la precisione del puntatore.<br/>                                                                             |
| <span id="HALF_PTR"></span><span id="half_ptr"></span>**METÀ \_ ptr**<br/>    | Metà delle dimensioni di un puntatore. Utilizzare all'interno di una struttura che contiene un puntatore e due campi di piccole dimensioni.<br/>                      |
| <span id="INT_PTR"></span><span id="int_ptr"></span>**\_ptr int**<br/>       | Tipo signed integer per la precisione del puntatore.<br/>                                                                            |
| <span id="LONG_PTR"></span><span id="long_ptr"></span>**LONG \_ ptr**<br/>    | Tipo Long firmato per la precisione del puntatore.<br/>                                                                               |
| <span id="SIZE_T"></span><span id="size_t"></span>**DIMENSIONI \_ T**<br/>          | Numero massimo di byte a cui può fare riferimento un puntatore. Utilizzare per un conteggio che deve estendersi all'intervallo completo di un puntatore.<br/> |
| <span id="SSIZE_T"></span><span id="ssize_t"></span>**SSIZE \_ T**<br/>       | Dimensioni con segno **\_ T**.<br/>                                                                                                   |
| <span id="UHALF_PTR"></span><span id="uhalf_ptr"></span>**UHALF \_ ptr**<br/> | **Metà \_ ptr** senza segno.<br/>                                                                                               |
| <span id="UINT_PTR"></span><span id="uint_ptr"></span>**\_ptr uint**<br/>    | **\_ Ptr int** senza segno.<br/>                                                                                                |
| <span id="ULONG_PTR"></span><span id="ulong_ptr"></span>**\_ptr ULONG**<br/> | **Long \_ ptr** senza segno.<br/>                                                                                               |



 

## <a name="specific-pointer-precision-types"></a>Tipi di Pointer-Precision specifici

I nuovi tipi di puntatore seguenti ridimensionano in modo esplicito il puntatore. Prestare attenzione quando si usano i puntatori nel codice a 64 bit: se si dichiara il puntatore usando un tipo a 32 bit, il sistema operativo crea il puntatore troncando un puntatore a 64 bit. Tutti i puntatori sono 64 bit in Windows a 64 bit.



| Termine                                                                                 | Descrizione                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="POINTER_32"></span><span id="pointer_32"></span>**PUNTATORE \_ 32**<br/> | Puntatore a 32 bit. In Windows a 32 bit, si tratta di un puntatore nativo. In Windows a 64 bit si tratta di un puntatore a 64 bit troncato.<br/>                                                                                       |
| <span id="POINTER_64"></span><span id="pointer_64"></span>**PUNTATORE \_ 64**<br/> | Puntatore a 64 bit. In Windows a 64 bit, si tratta di un puntatore nativo. In Windows a 32 bit si tratta di un puntatore a 32 bit esteso con segno. <br/> Si noti che non è sicuro presupporre lo stato del bit del puntatore elevato.<br/> |



 

 

