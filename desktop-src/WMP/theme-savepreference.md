---
title: THEME.savePreference
description: Il metodo savePreference salva una preferenza nel Registro di sistema.
ms.assetid: 4c253d8d-15c0-4c18-bb3f-fdbcef79c999
keywords:
- THEME.savePreference Windows Media Player
topic_type:
- apiref
api_name:
- THEME.savePreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d5f9edca154ff6402028ba873c1643e330ab316a54a63f14fa4f9b5bdb244483
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134544"
---
# <a name="themesavepreference"></a>THEME.savePreference

Il **metodo savePreference** salva una preferenza nel Registro di sistema.

``` syntax
        theme.savePreference(theKey, theValue)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*
</dt> <dd>

Valore **String** che specifica la chiave del valore di preferenza da salvare.

</dd> <dt>

<span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*theValue*
</dt> <dd>

Valore **String** che specifica il valore da salvare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Una preferenza è una coppia chiave/valore che può essere archiviata nel Registro di sistema per mantenere le informazioni sullo stato Windows Media Player tra le esecuzioni. Questa funzionalità può essere usata, ad esempio, per salvare le impostazioni di personalizzazione in modo che non sia necessario immettere di nuovo ogni volta Windows Media Player viene avviato.

Le preferenze non sono crittografate e pertanto non sono un metodo sicuro per rendere persistenti i dati. Non usare le preferenze per archiviare i dati privati.

## <a name="examples"></a>Esempio


```JScript
<THEME>
  <VIEW 
    id="View1" 
    onclose="jscript:theme.savePreference('drawer1','open');
             theme.savePreference('drawer2','close')">
  </VIEW>
</THEME>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> <dt>

[**THEME.loadPreference**](theme-loadpreference.md)
</dt> </dl>

 

 





