---
title: Metodi di proprietà IADsNameTranslate (IADs. h)
description: Imposta la proprietà ChaseReferral.
ms.assetid: 7c44fe9b-16a5-4bd5-a80b-8f3dcfec20cc
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsNameTranslate ADSI
topic_type:
- apiref
api_name:
- IADsNameTranslate Property Methods
- IADsNameTranslate.ChaseReferral
- IADsNameTranslate.put_ChaseReferral
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b90d068da3b8dca1bbcae361d1dbacafcf44464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964659"
---
# <a name="iadsnametranslate-property-methods"></a>Metodi di proprietà IADsNameTranslate

Il metodo Property dell'interfaccia [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) imposta la proprietà **ChaseReferral** . Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**ChaseReferral**
</dt> <dd> <dl>

Opzioni di ricerca dei riferimenti come definito in [**Ads \_ Chase \_ rinvii \_ enum**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum). Quando viene impostata l'indicizzazione del riferimento, la conversione del nome viene eseguita sugli oggetti che non appartengono a questa directory e sono i riferimenti restituiti dalla ricerca dei riferimenti.

<dt>

Tipo di accesso: sola scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT put_ChaseReferral(
  [in] LONG lnChaseReferral
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Commenti

Le opzioni di Chasing per il riferimento si applicano solo quando si usano [**IADsNameTranslate:: set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) e [**IADsNameTranslate:: Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get). La funzionalità non è disponibile con [**IADsNameTranslate:: SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex) o [**IADsNameTranslate:: GetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex).

L'interfaccia [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) ha un'implementazione parziale di [**Ads \_ Chase \_ referrals \_ enum**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) tramite la proprietà **ChaseReferral** . Se la proprietà **ChaseReferral** è impostata su zero (0), equivale a specificare i **\_ riferimenti Chase di ADS \_ \_ mai** (0). Se viene usato un valore diverso da zero, equivale a specificare i **\_ riferimenti Chase di ADS \_ \_ Always** (0x60). **IADsNameTranslate** non implementa le opzioni **Ads \_ Chase \_ \_ subordinate** (0x20) o **Ads \_ Chase \_ \_ External** (0x40).

L'impostazione predefinita per l'inseguimento dei riferimenti è abilitata (**Ads \_ Chase si \_ riferisce \_ sempre**). Senza la ricerca di riferimenti, è possibile eseguire la conversione dei nomi su tali oggetti che risiedono solo nel server di directory connesso. Se non si è certi che l'oggetto di interesse si trovi nel server specificato, è necessario impostare questa proprietà in modo che sia **\_ \_ \_ sempre ADS Chase referrals**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsNameTranslate è definito come B1B272A3-3625-11D1-A3A4-00C04FB950DC<br/>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_enumerazione riferimenti inseguiti Ads \_ \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)
</dt> <dt>

[**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)
</dt> <dt>

[**IADsNameTranslate:: Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get)
</dt> <dt>

[**IADsNameTranslate::GetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex)
</dt> <dt>

[**IADsNameTranslate:: set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set)
</dt> <dt>

[**IADsNameTranslate:: SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex)
</dt> <dt>

[Metodi di proprietà dell'interfaccia](interface-property-methods.md)
</dt> </dl>

 

 





