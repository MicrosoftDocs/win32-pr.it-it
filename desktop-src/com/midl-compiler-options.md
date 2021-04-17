---
title: Opzioni del compilatore MIDL
description: Opzioni del compilatore MIDL
ms.assetid: a78505cf-cda6-4b41-abd1-2609aec4dcb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e219daa345ad3140b78db8fdfc3de1d28678120
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339382"
---
# <a name="midl-compiler-options"></a>Opzioni del compilatore MIDL

È possibile usare le seguenti opzioni della riga di comando per eseguire l'override di alcuni dei comportamenti predefiniti del compilatore MIDL e per scegliere le ottimizzazioni appropriate per l'applicazione. Per un elenco completo delle opzioni della riga di comando MIDL, vedere il [riferimento a midl Command-Line](/windows/desktop/Midl/midl-command-line-reference).



| Switch della riga di comando                                       | Descrizione                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**/acf**](/windows/desktop/Midl/-acf)<br/>                          | Usare per fornire un nome file ACF esplicito. Questa opzione consente inoltre l'utilizzo di nomi di interfaccia diversi nei file IDL e ACF.<br/>                                                                                                       |
| [**/dlldata**](/windows/desktop/Midl/-dlldata)<br/>                  | Specifica un nome file per il file di dati DLL generato per una DLL proxy. Il nome file predefinito è dlldata. c.<br/>                                                                                                                              |
| [**/ENV**](/windows/desktop/Midl/-env)<br/>                          | Indica a MIDL di generare stub o una libreria dei tipi per un ambiente di destinazione.<br/>                                                                                                                                                            |
| [**/header**](/windows/desktop/Midl/-header), [ **/h**](/windows/desktop/Midl/-h)<br/> | Specifica il nome del file di intestazione dell'interfaccia. Il nome predefinito è quello del file IDL con estensione h.<br/>                                                                                                                       |
| [**/IID**](/windows/desktop/Midl/-iid)<br/>                          | Specifica un nome file dell'identificatore di interfaccia che sostituisce il nome file dell'identificatore di interfaccia predefinito per un'interfaccia COM.<br/>                                                                                                              |
| [**/LCID**](/windows/desktop/Midl/-lcid)<br/>                        | Fornisce supporto DBCS completo che consente di utilizzare i caratteri internazionali nei file di input, nei nomi di file e nei percorsi di directory.<br/>                                                                                                          |
| [**/No \_ Format \_ opz**](/windows/desktop/Midl/-no-format-opt)<br/>    | Per impostazione predefinita, per ridurre le dimensioni del codice, MIDL Elimina i descrittori duplicati. Questa opzione disattiva il comportamento di ottimizzazione.<br/>                                                                                                               |
| [**/OI**](/windows/desktop/Midl/-oi), **/OIC**, **/OIF**<br/>        | Indica a MIDL di usare un metodo di marshalling completamente interpretato. Le opzioni/OIC e/Oicf forniscono ulteriori miglioramenti delle prestazioni.<br/>                                                                                                   |
| [**/out**](/windows/desktop/Midl/-out)<br/>                          | Specifica la directory in cui il compilatore MIDL scrive i file di output. La directory di output può essere specificata con una lettera di unità, un percorso assoluto o entrambi. Il valore predefinito è che MIDL scrive i file nella directory corrente.<br/> |
| [**/proxy**](/windows/desktop/Midl/-proxy)<br/>                      | Specifica il nome del file proxy di interfaccia per un'interfaccia COM. Il nome predefinito è quello del file IDL più " \_ p. c".<br/>                                                                                                            |
| [**/TLB**](/windows/desktop/Midl/-tlb)<br/>                          | Specifica il nome del file di libreria dei tipi. Il nome predefinito è quello del file IDL con estensione tlb.<br/>                                                                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione MIDL](midl-compilation.md)
</dt> </dl>

 

