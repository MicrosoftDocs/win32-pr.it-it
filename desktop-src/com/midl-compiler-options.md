---
title: Opzioni del compilatore MIDL
description: Opzioni del compilatore MIDL
ms.assetid: a78505cf-cda6-4b41-abd1-2609aec4dcb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 649cd96ffc0afa171ad218a737910ce15facbe0e9b5ef302dedb6615228bcf3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859331"
---
# <a name="midl-compiler-options"></a>Opzioni del compilatore MIDL

È possibile usare le opzioni della riga di comando seguenti per eseguire l'override di alcuni comportamenti predefiniti del compilatore MIDL e per scegliere le ottimizzazioni appropriate per l'applicazione. Per un elenco completo delle opzioni della riga di comando MIDL, vedere MIDL Command-Line Reference (Informazioni di riferimento [su MIDL).](/windows/desktop/Midl/midl-command-line-reference)



| Switch della riga di comando                                       | Descrizione                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**/acf**](/windows/desktop/Midl/-acf)<br/>                          | Usare per specificare un nome file ACF esplicito. Questa opzione consente anche l'uso di nomi di interfaccia diversi nei file IDL e ACF.<br/>                                                                                                       |
| [**/dlldata**](/windows/desktop/Midl/-dlldata)<br/>                  | Specifica un nome file per il file di dati DLL generato per una DLL proxy. Il nome file predefinito è Dlldata.c.<br/>                                                                                                                              |
| [**/env**](/windows/desktop/Midl/-env)<br/>                          | Indica a MIDL di generare stub o una libreria dei tipi per un ambiente di destinazione.<br/>                                                                                                                                                            |
| [**/header**](/windows/desktop/Midl/-header), [ **/h**](/windows/desktop/Midl/-h)<br/> | Specifica il nome del file di intestazione dell'interfaccia. Il nome predefinito è quello del file IDL con estensione h.<br/>                                                                                                                       |
| [**/iid**](/windows/desktop/Midl/-iid)<br/>                          | Specifica un nome file dell'identificatore di interfaccia che esegue l'override del nome file dell'identificatore di interfaccia predefinito per un'interfaccia COM.<br/>                                                                                                              |
| [**/lcid**](/windows/desktop/Midl/-lcid)<br/>                        | Fornisce supporto DBCS completo per poter usare caratteri internazionali nei file di input, nei nomi file e nei percorsi di directory.<br/>                                                                                                          |
| [**/no \_ format \_ opt**](/windows/desktop/Midl/-no-format-opt)<br/>    | Per impostazione predefinita, per ridurre le dimensioni del codice, MIDL elimina i descrittori duplicati. Questa opzione disattiva questo comportamento di ottimizzazione.<br/>                                                                                                               |
| [**/Oi**](/windows/desktop/Midl/-oi), **/Oic**, **/Oif**<br/>        | Indica a MIDL di usare un metodo di marshalling completamente interpretato. Le opzioni /Oic e /Oicf offrono ulteriori miglioramenti delle prestazioni.<br/>                                                                                                   |
| [**/out**](/windows/desktop/Midl/-out)<br/>                          | Specifica la directory in cui il compilatore MIDL scrive i file di output. La directory di output può essere specificata con una lettera di unità, un percorso assoluto o entrambi. Il valore predefinito è che MIDL scrive i file nella directory corrente.<br/> |
| [**/proxy**](/windows/desktop/Midl/-proxy)<br/>                      | Specifica il nome del file proxy di interfaccia per un'interfaccia COM. Il nome predefinito è quello del file IDL più " \_ p.c".<br/>                                                                                                            |
| [**/tlb**](/windows/desktop/Midl/-tlb)<br/>                          | Specifica il nome del file di libreria dei tipi. Il nome predefinito è quello del file IDL, con estensione tlb.<br/>                                                                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione MIDL](midl-compilation.md)
</dt> </dl>

 

