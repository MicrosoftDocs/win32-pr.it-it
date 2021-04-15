---
title: Messaggio HKM_SETRULES (COMmctrl. h)
description: Definisce le combinazioni non valide e la combinazione di modificatore predefinita per un controllo tasto di scelta.
ms.assetid: de3dd463-a534-4c7c-ae04-da80a3bff2ab
keywords:
- Controlli di Windows Message HKM_SETRULES
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
ms.openlocfilehash: c33c0918a7bb44fdac9a1f2c60fdde8e06b5e679
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477296"
---
# <a name="hkm_setrules-message"></a>\_Messaggio regole di HKM

Definisce le combinazioni non valide e la combinazione di modificatore predefinita per un controllo tasto di scelta.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Matrice di flag che specificano combinazioni di chiavi non valide. Questo parametro può essere una combinazione dei valori seguenti:



| Valore                                                                                                                                                   | Significato                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="HKCOMB_A"></span><span id="hkcomb_a"></span><dl> <dt>**HKCOMB \_**</dt> </dl>          | ALT<br/>             |
| <span id="HKCOMB_C"></span><span id="hkcomb_c"></span><dl> <dt>**HKCOMB \_ C**</dt> </dl>          | CTRL<br/>            |
| <span id="HKCOMB_CA"></span><span id="hkcomb_ca"></span><dl> <dt>**\_CA HKCOMB**</dt> </dl>       | CTRL + ALT<br/>        |
| <span id="HKCOMB_NONE"></span><span id="hkcomb_none"></span><dl> <dt>**HKCOMB \_ None**</dt> </dl> | Chiavi non modificate<br/> |
| <span id="HKCOMB_S"></span><span id="hkcomb_s"></span><dl> <dt>**HKCOMB \_ S**</dt> </dl>          | MAIUSC<br/>           |
| <span id="HKCOMB_SA"></span><span id="hkcomb_sa"></span><dl> <dt>**\_sa HKCOMB**</dt> </dl>       | MAIUSC+ALT<br/>       |
| <span id="HKCOMB_SC"></span><span id="hkcomb_sc"></span><dl> <dt>**\_SC HKCOMB**</dt> </dl>       | MAIUSC + CTRL<br/>      |
| <span id="HKCOMB_SCA"></span><span id="hkcomb_sca"></span><dl> <dt>**HKCOMB \_ SCA**</dt> </dl>    | MAIUSC + CTRL + ALT<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Matrice di flag che specificano la combinazione di tasti da utilizzare quando l'utente immette una combinazione non valida. Per un elenco di valori dei flag di modifica, vedere la descrizione del messaggio [**\_ GetHotKey HKM**](hkm-gethotkey.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Quando un utente immette una combinazione di chiavi non valida, come definito dai flag specificati in *wParam*, il sistema usa l'operatore OR bit per bit per combinare le chiavi immesse dall'utente con i flag specificati in *lParam*. La combinazione di tasti risultante viene convertita in una stringa e quindi visualizzata nel controllo tasto di scelta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





