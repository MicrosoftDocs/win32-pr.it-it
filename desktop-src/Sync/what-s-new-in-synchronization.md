---
description: Windows include i nuovi elementi di programmazione seguenti per la sincronizzazione.
ms.assetid: 16cd98d2-adc5-4a14-ad39-a0c5b4cc00cc
title: Novità della sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4702ba10126d9c0eeeb85462195680b074918584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231691"
---
# <a name="whats-new-in-synchronization"></a>Novità della sincronizzazione

Windows include i nuovi elementi di programmazione seguenti per la sincronizzazione.

## <a name="windows-8"></a>Windows 8

### <a name="new-functions"></a>Funzioni nuove

<dl> <dt>

[**DeleteSynchronizationBarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier)
</dt> <dd>

Elimina una barriera di sincronizzazione.

</dd> <dt>

[**EnterSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

Fa in modo che il thread chiamante attenda una barriera di sincronizzazione finché il numero massimo di thread non è entrato nella barriera.

</dd> <dt>

[**GetOverlappedResultEx**](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex)
</dt> <dd>

Recupera i risultati di un'operazione sovrapposta sul file, named pipe o sul dispositivo di comunicazione specificato entro l'intervallo di timeout specificato. Il thread chiamante può eseguire un'attesa di avviso.

</dd> <dt>

[**InitializeSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

Specifica il numero massimo di thread e il numero di spin per una nuova barriera di sincronizzazione.

</dd> <dt>

[**WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress)
</dt> <dd>

Attende la modifica del valore in corrispondenza dell'indirizzo specificato.

</dd> <dt>

[**WakeByAddressAll**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall)
</dt> <dd>

Attiva tutti i thread in attesa che il valore di un indirizzo venga modificato.

</dd> <dt>

[**WakeByAddressSingle**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle)
</dt> <dd>

Attiva un thread in attesa della modifica del valore di un indirizzo.

</dd> </dl>

### <a name="new-interlocked-functions"></a>Nuove funzioni Interlocked

<dl> <dt>

[**InterlockedAddNoFence**](/previous-versions/windows/desktop/legacy/hh972629(v=vs.85))
</dt> <dd>

Esegue un'operazione di addizione atomica sui valori **Long** specificati. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972630(v=vs.85))
</dt> <dd>

Esegue un'operazione di addizione atomica sui valori **LONGLONG** specificati. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedAndNoFence**](/previous-versions/windows/desktop/legacy/hh972634(v=vs.85))
</dt> <dd>

Esegue un'operazione atomica e sui valori **Long** specificati. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedAnd8NoFence**](/previous-versions/windows/desktop/legacy/hh972633(v=vs.85))
</dt> <dd>

Esegue un'operazione atomica e sui valori **char** specificati. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedAnd16NoFence**](/previous-versions/windows/desktop/legacy/hh972631(v=vs.85))
</dt> <dd>

Esegue un'operazione atomica e sui valori **short** specificati. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedAnd64NoFence**](/previous-versions/windows/desktop/legacy/hh972632(v=vs.85))
</dt> <dd>

Esegue un'operazione atomica e sui valori **LONGLONG** specificati. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedBitTestAndComplement64**](/previous-versions/windows/desktop/legacy/hh972635(v=vs.85))
</dt> <dd>

Verifica il bit specificato del valore **long64** specificato e lo integra. L'operazione è atomica.

</dd> <dt>

[**InterlockedBitTestAndResetAcquire**](/previous-versions/windows/desktop/legacy/hh972636(v=vs.85))
</dt> <dd>

Verifica il bit specificato del valore **Long** specificato e lo imposta su 0. L'operazione è atomica e viene eseguita con la semantica di acquisizione dell'ordine di memoria.

</dd> <dt>

[**InterlockedBitTestAndResetRelease**](/previous-versions/windows/desktop/legacy/hh972637(v=vs.85))
</dt> <dd>

Verifica il bit specificato del valore **Long** specificato e lo imposta su 0. L'operazione è atomica e viene eseguita utilizzando la semantica di rilascio della memoria.

</dd> <dt>

[**InterlockedBitTestAndSetAcquire**](/previous-versions/windows/desktop/legacy/hh972638(v=vs.85))
</dt> <dd>

Verifica il bit specificato del valore **Long** specificato e lo imposta su 1. L'operazione è atomica e viene eseguita con la semantica di acquisizione dell'ordine di memoria.

</dd> <dt>

[**InterlockedBitTestAndSetRelease**](/previous-versions/windows/desktop/legacy/hh972639(v=vs.85))
</dt> <dd>

Verifica il bit specificato del valore **Long** specificato e lo imposta su 1. L'operazione è atomica e viene eseguita con la semantica di ordinamento della memoria di rilascio.

</dd> <dt>

[**InterlockedCompareExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972645(v=vs.85))
</dt> <dd>

Esegue un'operazione di confronto e scambio atomica sui valori specificati. La funzione Confronta due valori a 32 bit specificati e scambia con un altro valore a 32 bit in base al risultato del confronto. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedCompareExchange16**](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange16)
</dt> <dd>

Esegue un'operazione di confronto e scambio atomica sui valori specificati. La funzione Confronta due valori a 16 bit specificati e scambia con un altro valore a 16 bit in base al risultato del confronto.

</dd> <dt>

[**InterlockedCompareExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972642(v=vs.85))
</dt> <dd>

Esegue un'operazione di confronto e scambio atomica sui valori specificati. La funzione Confronta due valori a 16 bit specificati e scambia con un altro valore a 16 bit in base al risultato del confronto. L'operazione viene eseguita con la semantica di ordinamento della memoria acquisita.

</dd> <dt>

[**InterlockedCompareExchange16Release**](/previous-versions/windows/desktop/legacy/hh972644(v=vs.85))
</dt> <dd>

Esegue un'operazione di confronto e scambio atomica sui valori specificati. La funzione Confronta due valori a 16 bit specificati e scambia con un altro valore a 16 bit in base al risultato del confronto. Lo scambio viene eseguito con la semantica di ordinamento della memoria di rilascio.

</dd> <dt>

[**InterlockedCompareExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972643(v=vs.85))
</dt> <dd>

Esegue un'operazione di confronto e scambio atomica sui valori specificati. La funzione Confronta due valori a 16 bit specificati e scambia con un altro valore a 16 bit in base al risultato del confronto. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedCompareExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972646(v=vs.85))
</dt> <dd>

Esegue un'operazione di confronto e scambio atomica sui valori specificati. La funzione Confronta due valori a 64 bit specificati e scambia con un altro valore a 64 bit in base al risultato del confronto. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedCompareExchange128**](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange128)
</dt> <dd>

Esegue un'operazione di confronto e scambio atomica sui valori specificati. La funzione Confronta due valori a 128 bit specificati e scambia con un altro valore a 128 bit in base al risultato del confronto.

</dd> <dt>

[**InterlockedCompareExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972647(v=vs.85))
</dt> <dd>

Esegue un'operazione di confronto e scambio atomica sui valori specificati. La funzione Confronta due valori di puntatore e scambi specificati con un altro valore del puntatore in base al risultato del confronto. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedDecrementNoFence**](/previous-versions/windows/desktop/legacy/hh972652(v=vs.85))
</dt> <dd>

Decrementa (diminuisce di uno) il valore della variabile a 32 bit specificata come operazione atomica. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedDecrement16**](/windows/desktop/api/Winnt/nf-winnt-interlockeddecrement16)
</dt> <dd>

Decrementa (diminuisce di uno) il valore della variabile a 16 bit specificata come operazione atomica.

</dd> <dt>

[**InterlockedDecrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972649(v=vs.85))
</dt> <dd>

Decrementa (diminuisce di uno) il valore della variabile a 16 bit specificata come operazione atomica. L'operazione viene eseguita con la semantica di ordinamento della memoria acquisita.

</dd> <dt>

[**InterlockedDecrement16Release**](/previous-versions/windows/desktop/legacy/hh972651(v=vs.85))
</dt> <dd>

Decrementa (diminuisce di uno) il valore della variabile a 16 bit specificata come operazione atomica. L'operazione viene eseguita con la semantica di ordinamento della memoria di rilascio.

</dd> <dt>

[**InterlockedDecrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972650(v=vs.85))
</dt> <dd>

Decrementa (diminuisce di uno) il valore della variabile a 16 bit specificata come operazione atomica. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedDecrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972653(v=vs.85))
</dt> <dd>

Decrementa (diminuisce di uno) il valore della variabile a 64 bit specificata come operazione atomica. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972659(v=vs.85))
</dt> <dd>

Imposta una variabile a 64 bit sul valore specificato come operazione atomica. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedExchange8**](/windows/desktop/api/Winnt/nf-winnt-interlockedexchange8)
</dt> <dd>

Imposta una variabile a 8 bit sul valore specificato come operazione atomica.

</dd> <dt>

[**InterlockedExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972654(v=vs.85))
</dt> <dd>

Imposta una variabile a 16 bit sul valore specificato come operazione atomica. L'operazione viene eseguita usando la semantica di acquisizione dell'ordine di memoria.

</dd> <dt>

[**InterlockedExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972655(v=vs.85))
</dt> <dd>

Imposta una variabile a 16 bit sul valore specificato come operazione atomica. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972660(v=vs.85))
</dt> <dd>

Imposta una variabile a 64 bit sul valore specificato come operazione atomica. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972661(v=vs.85))
</dt> <dd>

Scambia atomicamente una coppia di indirizzi. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedExchangeAddNoFence**](/previous-versions/windows/desktop/legacy/hh972657(v=vs.85))
</dt> <dd>

Esegue un'aggiunta atomica di valori a 2 32 bit. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedExchangeAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972658(v=vs.85))
</dt> <dd>

Esegue un'aggiunta atomica di valori a 2 64 bit. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedIncrementNoFence**](/previous-versions/windows/desktop/legacy/hh972667(v=vs.85))
</dt> <dd>

Incrementa (aumenta di uno) il valore della variabile a 32 bit specificata come operazione atomica. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedIncrement16**](/windows/desktop/api/Winnt/nf-winnt-interlockedincrement16)
</dt> <dd>

Incrementa (aumenta di uno) il valore della variabile a 16 bit specificata come operazione atomica.

</dd> <dt>

[**InterlockedIncrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972663(v=vs.85))
</dt> <dd>

Incrementa (aumenta di uno) il valore della variabile a 16 bit specificata come operazione atomica. L'operazione viene eseguita usando la semantica di acquisizione dell'ordine di memoria.

</dd> <dt>

[**InterlockedIncrement16Release**](/previous-versions/windows/desktop/legacy/hh972665(v=vs.85))
</dt> <dd>

Incrementa (aumenta di uno) il valore della variabile a 16 bit specificata come operazione atomica. L'operazione viene eseguita usando la semantica di ordinamento della memoria di rilascio.

</dd> <dt>

[**InterlockedIncrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972664(v=vs.85))
</dt> <dd>

Incrementa (aumenta di uno) il valore della variabile a 16 bit specificata come operazione atomica. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedIncrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972668(v=vs.85))
</dt> <dd>

Incrementa (aumenta di uno) il valore della variabile a 64 bit specificata come operazione atomica. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedOrNoFence**](/previous-versions/windows/desktop/legacy/hh972672(v=vs.85))
</dt> <dd>

Esegue un'operazione atomica o sui valori **Long** specificati. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedOr8NoFence**](/previous-versions/windows/desktop/legacy/hh972671(v=vs.85))
</dt> <dd>

Esegue un'operazione atomica o sui valori **char** specificati. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedOr16NoFence**](/previous-versions/windows/desktop/legacy/hh972669(v=vs.85))
</dt> <dd>

Esegue un'operazione atomica o sui valori **short** specificati. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedOr64NoFence**](/previous-versions/windows/desktop/legacy/hh972670(v=vs.85))
</dt> <dd>

Esegue un'operazione atomica o sui valori **LONGLONG** specificati. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedPushListSListEx**](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)
</dt> <dd>

Inserisce un elenco collegato singolarmente davanti a un altro elenco collegato singolarmente. L'accesso agli elenchi è sincronizzato in un sistema multiprocessore. Questa versione del metodo non usa la convenzione di chiamata [ \_ \_ fastcall](https://msdn.microsoft.com/library/6xa169sk(v=VS.71).aspx) .

</dd> <dt>

[**InterlockedXorNoFence**](/previous-versions/windows/desktop/legacy/hh972677(v=vs.85))
</dt> <dd>

Esegue un'operazione Atomic XOR sui valori **Long** specificati. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedXor8NoFence**](/previous-versions/windows/desktop/legacy/hh972676(v=vs.85))
</dt> <dd>

Esegue un'operazione Atomic XOR sui valori **char** specificati. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedXor16NoFence**](/previous-versions/windows/desktop/legacy/hh972674(v=vs.85))
</dt> <dd>

Esegue un'operazione Atomic XOR sui valori **short** specificati. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> <dt>

[**InterlockedXor64NoFence**](/previous-versions/windows/desktop/legacy/hh972675(v=vs.85))
</dt> <dd>

Esegue un'operazione Atomic XOR sui valori **LONGLONG** specificati. L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.

</dd> </dl>

## <a name="windows-7"></a>Windows 7

### <a name="new-functions"></a>Funzioni nuove

<dl> <dt>

[**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)
</dt> <dd>

Attiva il timer di attesa specificato e fornisce informazioni sul contesto per il timer.

</dd> <dt>

[**TryAcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive)
</dt> <dd>

Tenta di acquisire un blocco di lettura/scrittura (SRW) Slim in modalità esclusiva. Se la chiamata ha esito positivo, il thread chiamante acquisisce la proprietà del blocco.

</dd> <dt>

[**TryAcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockshared)
</dt> <dd>

Tenta di acquisire un blocco di lettura/scrittura (SRW) Slim in modalità condivisa. Se la chiamata ha esito positivo, il thread chiamante acquisisce la proprietà del blocco.

</dd> </dl>

### <a name="new-structures"></a>Nuove strutture

<dl> <dt>

[**\_contesto motivo**](/windows/win32/api/minwinbase/ns-minwinbase-reason_context)
</dt> <dd>

Contiene informazioni di contesto per un timer attivato con [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex).

</dd> </dl>

 

 
