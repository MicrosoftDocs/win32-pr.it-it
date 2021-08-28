---
title: Nuovi tipi di dati
description: Sono state introdotte tre classi di tipi di dati per i tipi Windows a 64 bit, i tipi di dati a precisione fissa, i tipi di precisione del puntatore e i tipi di precisione del puntatore specifici.
ms.assetid: 016977d4-e7bf-463e-9755-7ef13f16e9e5
keywords:
- Guida alla programmazione a 64 bit Windows programmazione a 64 bit Windows programmazione di , tipi di dati
- tipi di dati programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc3cc6615de7c93c805eac868536b53084a694fb79d4e63d908716eb026eb71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504841"
---
# <a name="the-new-data-types"></a>Nuovi tipi di dati

Sono state introdotte tre classi di tipi di dati per il Windows a 64 bit: tipi di dati a precisione fissa, tipi di precisione del puntatore e tipi di precisione del puntatore specifici. Questi tipi sono stati aggiunti all'ambiente di sviluppo per consentire agli sviluppatori di prepararsi per le applicazioni a 64 bit Windows. Questi tipi derivano dai tipi integer e long in linguaggio C di base. Pertanto, è possibile usare questi tipi di dati nel codice compilato e testato in un Windows a 32 bit e quindi ricompilare con il compilatore a 64 bit quando la destinazione è Windows.

Anche per le applicazioni che hanno come destinazione solo Windows a 32 bit, l'adozione di questi nuovi tipi di dati rende il codice più affidabile. Per usare questi tipi di dati, è necessario analizzare il codice per l'utilizzo di puntatori potenzialmente non sicuri, il polimorfismo e le definizioni dei dati. Ad esempio, quando una variabile è di tipo **ULONG \_ PTR,** è chiaro che verrà usata per il cast dei puntatori per operazioni aritmetiche o polimorfismo. Non è possibile indicare tale utilizzo direttamente usando i tipi di dati meno recenti. È possibile eseguire questa operazione indirettamente usando la denominazione dei tipi derivati o la notazione ungherese, ma entrambe le tecniche sono erre erre.

Tutti questi tipi di dati vengono dichiarati in BaseTsd.h. Per altre informazioni, incluse le definizioni di questi tipi di dati, [vedere Windows di dati](/windows/desktop/WinProg/windows-data-types).

## <a name="fixed-precision"></a>Precisione fissa

I tipi di dati a precisione fissa hanno la stessa lunghezza nei tipi di dati a 32 e 64 bit Windows. Per ricordarlo, la precisione fa parte del nome del tipo di dati. Di seguito sono riportati i tipi di dati a precisione fissa.



| Termine                                                                       | Descrizione                        |
|----------------------------------------------------------------------------|------------------------------------|
| <span id="DWORD32"></span><span id="dword32"></span>**DWORD32**<br/> | Intero senza segno a 32 bit<br/> |
| <span id="DWORD64"></span><span id="dword64"></span>**DWORD64**<br/> | Intero senza segno a 64 bit<br/> |
| <span id="INT32"></span><span id="int32"></span>**INT32**<br/>       | Intero con segno a 32 bit<br/>   |
| <span id="INT64"></span><span id="int64"></span>**INT64**<br/>       | Intero con segno a 64 bit<br/>   |
| <span id="LONG32"></span><span id="long32"></span>**LONG32**<br/>    | Intero con segno a 32 bit<br/>   |
| <span id="LONG64"></span><span id="long64"></span>**LONG64**<br/>    | Intero con segno a 64 bit<br/>   |
| <span id="UINT32"></span><span id="uint32"></span>**UINT32**<br/>    | Unsigned **INT32**<br/>      |
| <span id="UINT64"></span><span id="uint64"></span>**UINT64**<br/>    | Unsigned **INT64**<br/>      |
| <span id="ULONG32"></span><span id="ulong32"></span>**Ulong32**<br/> | **LONG32 senza segno**<br/>     |
| <span id="ULONG64"></span><span id="ulong64"></span>**ULONG64**<br/> | **LONG64 senza segno**<br/>     |



 

## <a name="pointer-precision"></a>Precisione del puntatore

Quando la precisione del puntatore cambia (ovvero quando diventa a 32 bit in Windows a 32 bit e a 64 bit con Windows a 64 bit), i tipi di dati di precisione del puntatore riflettono la precisione di conseguenza. Pertanto, è sicuro eseguire il cast di un puntatore a uno di questi tipi quando si esegue l'aritmetica dei puntatori; se la precisione del puntatore è a 64 bit, il tipo è a 64 bit. I tipi di conteggio riflettono anche le dimensioni massime a cui un puntatore può fare riferimento. Di seguito sono riportati i tipi pointer-precision e count.



| Termine                                                                              | Descrizione                                                                                                                      |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span id="DWORD_PTR"></span><span id="dword_ptr"></span>**DWORD \_ PTR**<br/> | Tipo long senza segno per la precisione del puntatore.<br/>                                                                             |
| <span id="HALF_PTR"></span><span id="half_ptr"></span>**HALF \_ PTR**<br/>    | Metà delle dimensioni di un puntatore. Usare all'interno di una struttura che contiene un puntatore e due campi piccoli.<br/>                      |
| <span id="INT_PTR"></span><span id="int_ptr"></span>**INT \_ PTR**<br/>       | Tipo Signed Integer per la precisione del puntatore.<br/>                                                                            |
| <span id="LONG_PTR"></span><span id="long_ptr"></span>**LONG \_ PTR**<br/>    | Tipo long con segno per la precisione del puntatore.<br/>                                                                               |
| <span id="SIZE_T"></span><span id="size_t"></span>**DIMENSIONI \_ T**<br/>          | Numero massimo di byte a cui un puntatore può fare riferimento. Usare per un conteggio che deve estendersi all'intero intervallo di un puntatore.<br/> |
| <span id="SSIZE_T"></span><span id="ssize_t"></span>**SSIZE \_ T**<br/>       | Signed **SIZE \_ T**.<br/>                                                                                                   |
| <span id="UHALF_PTR"></span><span id="uhalf_ptr"></span>**UHALF \_ PTR**<br/> | HALF **PTR senza \_ segno.**<br/>                                                                                               |
| <span id="UINT_PTR"></span><span id="uint_ptr"></span>**UINT \_ PTR**<br/>    | Unsigned **INT \_ PTR**.<br/>                                                                                                |
| <span id="ULONG_PTR"></span><span id="ulong_ptr"></span>**ULONG \_ PTR**<br/> | Unsigned **LONG \_ PTR**.<br/>                                                                                               |



 

## <a name="specific-pointer-precision-types"></a>Tipi di Pointer-Precision specifici

I nuovi tipi di puntatore seguenti ridimensionano in modo esplicito il puntatore. Fare attenzione quando si usano puntatori nel codice a 64 bit: se si dichiara il puntatore usando un tipo a 32 bit, il sistema operativo crea il puntatore troncando un puntatore a 64 bit. Tutti i puntatori sono a 64 bit in Windows.



| Termine                                                                                 | Descrizione                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="POINTER_32"></span><span id="pointer_32"></span>**PUNTATORE \_ 32**<br/> | Puntatore a 32 bit. In caso di errore Windows a 32 bit, si tratta di un puntatore nativo. In caso di Windows a 64 bit, si tratta di un puntatore a 64 bit troncato.<br/>                                                                                       |
| <span id="POINTER_64"></span><span id="pointer_64"></span>**PUNTATORE \_ 64**<br/> | Puntatore a 64 bit. Nelle applicazioni a 64 bit Windows, si tratta di un puntatore nativo. Nelle applicazioni a 32 bit Windows, si tratta di un puntatore a 32 bit esteso con segno. <br/> Si noti che non è sicuro presupporre lo stato del bit del puntatore alto.<br/> |



 

 

