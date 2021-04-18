---
title: THEME. loadPreference
description: Il metodo loadPreference carica una preferenza dal registro di sistema.
ms.assetid: 51d6b0f8-f1fd-4999-a575-0b7c177b2bc8
keywords:
- THEME. loadPreference Windows Media Player
topic_type:
- apiref
api_name:
- THEME.loadPreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d92135113495ac32ca81f602ea5836332159164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333827"
---
# <a name="themeloadpreference"></a>THEME. loadPreference

Il metodo **loadPreference** carica una preferenza dal registro di sistema.

``` syntax
        theme.loadPreference(theKey)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*
</dt> <dd>

**Stringa** che specifica la chiave del valore di preferenza da caricare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce una **stringa**.

## <a name="remarks"></a>Commenti

Una preferenza è una coppia chiave/valore che può essere archiviata nel registro di sistema per mantenere le informazioni sullo stato del Media Player di Windows tra le esecuzioni. Questa funzionalità può essere usata, ad esempio, per salvare le impostazioni di personalizzazione in modo che non debbano essere immesse di nuovo ogni volta che viene avviato Windows Media Player.

Le preferenze non sono crittografate e pertanto non sono un metodo sicuro per rendere permanente i dati. Non usare le preferenze per archiviare i dati privati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> <dt>

[**THEME. savePreference**](theme-savepreference.md)
</dt> </dl>

 

 





