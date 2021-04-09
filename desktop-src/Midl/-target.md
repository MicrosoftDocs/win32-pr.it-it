---
title: opzione/target
description: L'opzione/target consente al compilatore MIDL di abilitare le ottimizzazioni disponibili solo nelle versioni recenti di Windows. Il commutatore/target attiva automaticamente opzioni aggiuntive.
ms.assetid: 8c5aa319-e6a6-4803-99f3-ed8751d565d5
keywords:
- Switch/target MIDL
topic_type:
- apiref
api_name:
- /target
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 43c17c6bb06eca94a1738ddc71255cd7cd441c5c
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "104058404"
---
# <a name="target-switch"></a>opzione/target

L'opzione **/target** consente al compilatore MIDL di abilitare le ottimizzazioni disponibili solo nelle versioni recenti di Windows. Il commutatore **/target** attiva automaticamente opzioni aggiuntive.

``` syntax
midl /target level
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*level* 
</dt> <dd>

Specifica il livello di destinazione, ad esempio NT50, NT51, NT60, NT61, NT62 o NT100.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il commutatore **/target** attiva automaticamente opzioni aggiuntive, in base al sistema operativo, come specificato nella tabella seguente:



| Sistema operativo | livello/target | Opzioni attivate                     |
|------------------|---------------|----------------------------------------|
| Windows 2000     | NT50          | /Oicf/Error tutti/robust               |
| Windows XP       | NT51          | /Oicf/error all/robust/Protocol all |
| Windows Vista    | NT60          | /Oicf/error all/robust/Protocol all |
| Windows 7        | NT61          | /Oicf/error all/robust/Protocol all |
| Windows 8        | NT62          | /Oicf/error all/robust/Protocol all |
| Windows 10       | NT100         | /Oicf/error all/robust/Protocol all |
 

Per assicurarsi che uno stub venga eseguito nel sistema specificato dall'opzione **/target** , MIDL genera un errore quando è presente una funzionalità disponibile solo in una versione più recente di Windows. Nella tabella seguente viene specificato il livello **/target** minimo necessario per abilitare la funzionalità. I livelli di destinazione più elevati includono tutte le funzionalità dei livelli di destinazione inferiori.



| Livello/target minimo richiesto | Funzionalità                                                                                                                                                                                          |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NT50                           | /Robust<br/> \[message\]<br/> \[async\]<br/> \[\_UUID asincrono\]<br/> \[notifica \] in modalità/Oicf<br/> \[codificare \] o \[ decodificare \] in modalità/Oicf<br/>                   |
| NT51                           | supporto/Protocol a 64 bit<br/> \[\_Ignora parziale\]<br/> \[forza \_ allocazione\]<br/>                                                                                                 |
| NT60                           | Marshalling della struttura complessa forzata<br/> Handle di contesto in una matrice o una struttura<br/> \[\]supporto dell'intervallo per le stringhe non dimensionate<br/> \[tipo \_ strict \_ handle di contesto \_\]<br/> |
| NT61                           | Le chiamate dirette a Stub COM per le interfacce con metodi inferiori a 32 richiedono il collegamento di stub COM con **OLE32.DLL**.<br/>                                                                          |
| NT62                           | Supporto ARM<br/> Supporto di WinRT<br/>                                                                                                                                                   |
| NT100                          | \[\]supporto system_handle<br /> |


 

## <a name="examples"></a>Esempio

**NT50/target MIDL**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>
