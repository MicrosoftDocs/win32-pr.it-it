---
title: Opzione /Oi
description: Le opzioni /Oi e /Oic indirizzano il compilatore MIDL all'uso di un metodo di marshalling completamente interpretato. L'opzione /Oicf offre miglioramenti aggiuntivi per le prestazioni.
ms.assetid: cf597a45-410f-4098-850b-240c6ebce23b
keywords:
- Opzione /Oi MIDL
topic_type:
- apiref
api_name:
- /Oi
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f38b6faee202e15b7c551297678ce301cbfdcb853b48ecd15c75dda7bb281e72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385285"
---
# <a name="oi-switch"></a>Opzione /Oi

Le **opzioni /Oi** e **/Oic** indirizzano il compilatore MIDL all'uso di un metodo di marshalling completamente interpretato. **L'opzione /Oicf** offre miglioramenti aggiuntivi per le prestazioni.

``` syntax
midl /{Oi | Oic | Oif | Oicf}
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*Oi* 
</dt> <dd>

Specifica il metodo completamente interpretato per il marshalling del codice stub passato tra client e server.

> [!Note]  
> Questa opzione è obsoleta. È consigliabile usare **l'opzione /Oicf** al suo posto.

 

</dd> <dt>

*Oic* 
</dt> <dd>

Specifica il metodo proxy senza codice di marshalling che fornisce tutte le funzionalità di **/Oi** e riduce ulteriormente le dimensioni del codice stub client per le interfacce oggetto.

> [!Note]  
> Questa opzione è obsoleta. È consigliabile usare **l'opzione /Oicf** al suo posto.

 

</dd> <dt>

*Oif o Oicf* 
</dt> <dd>

Specifica il metodo proxy senza codice di marshalling che include tutte le funzionalità fornite da **/Oi** e **/Oic,** ma usa un nuovo interprete (stringhe di formato rapido) che offre prestazioni migliori rispetto a **/Oi** o **/Oic**. Questa opzione include miglioramenti rpc recenti ed è consigliata per gli scenari RPC moderni.

</dd> </dl>

## <a name="remarks"></a>Commenti

Si notino le restrizioni relative alle piattaforme di supporto.

Il compilatore MIDL 3.0 fornisce due metodi per il marshalling del codice: completamente interpretato ( **/Oi**, **/Oic** e **/Oicf**) e in modalità mista ( [**/Os**](-os.md)). A partire da MIDL versione 6.0.359, il compilatore MIDL genera **stub /Oicf** Â [**/robust**](-robust.md) per impostazione predefinita. Alcune funzionalità del linguaggio non sono supportate in alcune modalità. In questo caso, il compilatore passa automaticamente alla modalità appropriata e genera un avviso.

Se le prestazioni sono un problema, il metodo in modalità mista ( [**/Os**](-os.md)) può essere l'approccio migliore. In questa modalità, il compilatore sceglie di effettuare il marshalling di alcuni parametri inline negli stub generati. Anche se ciò comporta dimensioni di stub maggiori, offre prestazioni migliori.

Il metodo completamente interpretato effettua il marshalling dei dati completamente offline. In questo modo si riducono notevolmente le dimensioni del codice stub, ma si riducono le prestazioni. Inoltre, con il metodo completamente interpretato, è previsto un limite di 16 parametri per ogni procedura. Qualsiasi procedura contenente più di 16 parametri verrà elaborata automaticamente in [**modalità /Os.**](-os.md) Tra le modalità interpretate, **/Oicf** offre le migliori prestazioni e **/Oi** offre la migliore compatibilità con le versioni precedenti.

È possibile usare l'opzione **/Oif** se l'applicazione usa funzionalità MIDL introdotte con MIDL 3.0, ad esempio gli attributi \[ [**wire \_ marshal**](wire-marshal.md) e \] user \[ [**\_ marshal.**](user-marshal.md) \] Se l'applicazione [usa pipe,](/windows/desktop/Rpc/pipes) è necessario usare **l'opzione /Oif.** Se si specifica un'altra modalità, il compilatore MIDL passa **a /Oif**.

Per ottimizzare la modalità di marshalling del codice stub, RPC Microsoft fornisce un attributo di ottimizzazione \[ [](optimize.md) \] ACF. Questo attributo viene utilizzato come attributo di interfaccia o di operazione per selezionare la modalità di marshalling per singole interfacce o per singole operazioni.

### <a name="calling-conventions"></a>Convenzioni di chiamata

Gli stub generati dal compilatore MIDL nel metodo interpretato usando le opzioni **/Oi**, **/Oic** o **/Oif** devono essere compilati come routine stdcall o cdecl durante la compilazione C. Una convenzione di chiamata PASCAL o Fastcall non funzionerà. Inoltre, lo stub del server deve essere compilato come stdcall.

## <a name="examples"></a>Esempio

**midl /Oi filename.idl**

**midl /Oic filename.idl**

**midl /Oif filename.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**/robust**](-robust.md)
</dt> <dt>

[**/no \_ robust**](-no-robust.md)
</dt> <dt>

[Sintassi generale della riga di comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Os**](-os.md)
</dt> <dt>

[**Ottimizzare**](optimize.md)
</dt> <dt>

[**/no \_ format \_ opt**](-no-format-opt.md)
</dt> </dl>

 

 