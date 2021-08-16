---
title: HKM_SETRULES messaggio (Commctrl.h)
description: Definisce le combinazioni non valide e la combinazione di modificatori predefinita per un controllo tasto di scelta rapida.
ms.assetid: de3dd463-a534-4c7c-ae04-da80a3bff2ab
keywords:
- HKM_SETRULES dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- HKM_SETRULES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ec47450ca0d67854d7be413d8a3eb3e5fec3eac49e18f6bcf96f86b563c8906
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958710"
---
# <a name="hkm_setrules-message"></a>Messaggio \_ SETRULES HKM

Definisce le combinazioni non valide e la combinazione di modificatori predefinita per un controllo tasto di scelta rapida.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Matrice di flag che specificano combinazioni di tasti non valide. Questo parametro può essere una combinazione dei valori seguenti:



| Valore                                                                                                                                                   | Significato                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="HKCOMB_A"></span><span id="hkcomb_a"></span><dl> <dt>**HKCOMB \_ A**</dt> </dl>          | ALT<br/>             |
| <span id="HKCOMB_C"></span><span id="hkcomb_c"></span><dl> <dt>**HKCOMB \_ C**</dt> </dl>          | CTRL<br/>            |
| <span id="HKCOMB_CA"></span><span id="hkcomb_ca"></span><dl> <dt>**HKCOMB \_ CA**</dt> </dl>       | CTRL+ALT<br/>        |
| <span id="HKCOMB_NONE"></span><span id="hkcomb_none"></span><dl> <dt>**HKCOMB \_ NONE**</dt> </dl> | Chiavi non modificati<br/> |
| <span id="HKCOMB_S"></span><span id="hkcomb_s"></span><dl> <dt>**HKCOMB \_ S**</dt> </dl>          | Maiusc<br/>           |
| <span id="HKCOMB_SA"></span><span id="hkcomb_sa"></span><dl> <dt>**HKCOMB \_ SA**</dt> </dl>       | MAIUSC+ALT<br/>       |
| <span id="HKCOMB_SC"></span><span id="hkcomb_sc"></span><dl> <dt>**HKCOMB \_ SC**</dt> </dl>       | MAIUSC+CTRL<br/>      |
| <span id="HKCOMB_SCA"></span><span id="hkcomb_sca"></span><dl> <dt>**HKCOMB \_ SCA**</dt> </dl>    | MAIUSC+CTRL+ALT<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Matrice di flag che specificano la combinazione di tasti da usare quando l'utente immette una combinazione non valida. Per un elenco dei valori dei flag di modifica, vedere la descrizione del [**messaggio \_ HKM GETHOTKEY.**](hkm-gethotkey.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Quando un utente immette una combinazione di tasti non valida, come definito dai flag specificati in *wParam*, il sistema usa l'operatore OR bit per bit per combinare le chiavi immesse dall'utente con i flag specificati in *lParam*. La combinazione di tasti risultante viene convertita in una stringa e quindi visualizzata nel controllo tasto di scelta rapida.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





