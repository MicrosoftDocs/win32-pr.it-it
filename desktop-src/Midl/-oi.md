---
title: Opzione/Oi
description: Le opzioni/OI e/OIC indirizzano il compilatore MIDL per l'uso di un metodo di marshalling completamente interpretato. L'opzione/Oicf fornisce ulteriori miglioramenti delle prestazioni.
ms.assetid: cf597a45-410f-4098-850b-240c6ebce23b
keywords:
- /OI switch MIDL
topic_type:
- apiref
api_name:
- /Oi
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1671b16640d3f3214f10138e50a2ac08b6114674
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104223539"
---
# <a name="oi-switch"></a>Opzione/Oi

Le opzioni **/OI** e **/OIC** indirizzano il compilatore MIDL per l'uso di un metodo di marshalling completamente interpretato. L'opzione **/Oicf** fornisce ulteriori miglioramenti delle prestazioni.

``` syntax
midl /{Oi | Oic | Oif | Oicf}
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*OI* 
</dt> <dd>

Specifica il metodo completamente interpretato per il marshalling del codice stub passato tra client e server.

> [!Note]  
> Questa opzione è obsoleta. Si consiglia di usare l'opzione **/Oicf** al suo posto.

 

</dd> <dt>

*OIC* 
</dt> <dd>

Specifica il metodo proxy senza codice per il marshalling che fornisce tutte le funzionalità di **/OI** e riduce ulteriormente le dimensioni del codice stub client per le interfacce oggetto.

> [!Note]  
> Questa opzione è obsoleta. Si consiglia di usare l'opzione **/Oicf** al suo posto.

 

</dd> <dt>

*OIF o Oicf* 
</dt> <dd>

Specifica il metodo proxy senza codice del marshalling che include tutte le funzionalità fornite da **/OI** e **/OIC** , ma usa un nuovo interprete (stringhe di formato rapido) che offre prestazioni migliori rispetto a **/OI** o **/OIC**. Questa opzione include miglioramenti recenti di RPC ed è consigliata per gli scenari RPC moderni.

</dd> </dl>

## <a name="remarks"></a>Commenti

Si notino le restrizioni relative alle piattaforme di supporto.

Il compilatore MIDL 3,0 fornisce due metodi per il marshalling del codice: completamente interpretato ( **/OI**, **/OIC** e **/Oicf**) e in modalità mista ( [**/OS**](-os.md)). A partire dalla versione MIDL 6.0.359, il compilatore MIDL genera gli stub **/Oicf** Â  [**/robust**](-robust.md) per impostazione predefinita. Alcune funzionalità del linguaggio non sono supportate in alcune modalità. In questo caso, il compilatore passa automaticamente alla modalità appropriata e genera un avviso.

Se le prestazioni sono un problema, il metodo in modalità mista ( [**/OS**](-os.md)) può essere l'approccio migliore. In questa modalità, il compilatore sceglie di effettuare il marshalling di alcuni parametri inline negli stub generati. Sebbene il risultato sia una dimensione dello stub più grande, offre prestazioni migliori.

Il metodo completamente interpretato esegue il marshalling dei dati completamente offline. Questo consente di ridurre notevolmente le dimensioni del codice stub, ma comporta una riduzione delle prestazioni. Inoltre, con il metodo completamente interpretato, è previsto un limite di 16 parametri per ogni procedura. Qualsiasi routine contenente più di 16 parametri verrà automaticamente elaborata in modalità [**/OS**](-os.md) . Tra le modalità interpretate, **/Oicf** offre le migliori prestazioni e **/OI** offre la migliore compatibilità con le versioni precedenti.

È possibile usare l'opzione **/OIF** se l'applicazione usa le funzionalità MIDL introdotte con MIDL 3,0, ad esempio il \[ [**\_ marshalling di rete**](wire-marshal.md) \] e \[ gli attributi di [**\_ marshalling degli utenti**](user-marshal.md) \] . Se l'applicazione usa le [pipe](/windows/desktop/Rpc/pipes) , è necessario usare l'opzione **/OIF** . Se si specifica un'altra modalità, il compilatore MIDL passerà a **/OIF**.

Per ottimizzare la modalità di marshalling del codice stub, Microsoft RPC fornisce un attributo di \[ [**ottimizzazione**](optimize.md) ACF \] . Questo attributo viene utilizzato come attributo di interfaccia o attributo di operazione per selezionare la modalità di marshalling per le singole interfacce o per singole operazioni.

### <a name="calling-conventions"></a>Convenzioni di chiamata

Gli stub generati dal compilatore MIDL nel metodo interpretato mediante le opzioni **/OI**, **/OIC** o **/OIF** devono essere compilati come una routine stdcall o cdecl durante la compilazione C. Una convenzione di chiamata PASCAL o fastcall non funzionerà. Inoltre, lo stub del server deve essere compilato come stdcall.

## <a name="examples"></a>Esempio

**MIDL/OI nomefile. idl**

**MIDL/OIC nomefile. idl**

**MIDL/OIF nomefile. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**/Robust**](-robust.md)
</dt> <dt>

[**/No \_ affidabile**](-no-robust.md)
</dt> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/OS**](-os.md)
</dt> <dt>

[**ottimizzare**](optimize.md)
</dt> <dt>

[**/No \_ Format \_ opz**](-no-format-opt.md)
</dt> </dl>

 

 