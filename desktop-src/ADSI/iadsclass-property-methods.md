---
title: Metodi di proprietà IADsClass (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsClass ottengono o impostano le proprietà seguenti. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 191f6873-c4bd-4e71-9d23-478454b7cec2
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsClass ADSI
topic_type:
- apiref
api_name:
- IADsClass Property Methods
- IADsClass.Abstract
- IADsClass.get_Abstract
- IADsClass.put_Abstract
- IADsClass.AuxDerivedFrom
- IADsClass.get_AuxDerivedFrom
- IADsClass.put_AuxDerivedFrom
- IADsClass.Auxiliary
- IADsClass.get_Auxiliary
- IADsClass.put_Auxiliary
- IADsClass.CLSID
- IADsClass.get_CLSID
- IADsClass.put_CLSID
- IADsClass.Container
- IADsClass.get_Container
- IADsClass.put_Container
- IADsClass.Containment
- IADsClass.get_Containment
- IADsClass.put_Containment
- IADsClass.DerivedFrom
- IADsClass.get_DerivedFrom
- IADsClass.put_DerivedFrom
- IADsClass.HelpFileContext
- IADsClass.get_HelpFileContext
- IADsClass.put_HelpFileContext
- IADsClass.HelpFileName
- IADsClass.get_HelpFileName
- IADsClass.put_HelpFileName
- IADsClass.MandatoryProperties
- IADsClass.get_MandatoryProperties
- IADsClass.put_MandatoryProperties
- IADsClass.NamingProperties
- IADsClass.get_NamingProperties
- IADsClass.put_NamingProperties
- IADsClass.OID
- IADsClass.get_OID
- IADsClass.put_OID
- IADsClass.OptionalProperties
- IADsClass.get_OptionalProperties
- IADsClass.put_OptionalProperties
- IADsClass.PossibleSuperiors
- IADsClass.get_PossibleSuperiors
- IADsClass.put_PossibleSuperiors
- IADsClass.PrimaryInterface
- IADsClass.get_PrimaryInterface
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358bc33347f035af92303a4ce9879105cd247a3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120754"
---
# <a name="iadsclass-property-methods"></a>Metodi di proprietà IADsClass

I metodi di proprietà dell'interfaccia [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) ottengono o impostano le proprietà seguenti. Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**Contenuto**
</dt> <dd> <dl>

Valore booleano che indica se questa classe è astratta o non astratta. Se è **true**, questa classe è una classe astratta e non è possibile crearne un'istanza direttamente nel servizio directory. Le classi astratte possono essere utilizzate solo come classi super.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Boolean**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Abstract(
  [out] BOOLEAN* pbAbstract
);
HRESULT put_Abstract(
  [in] BOOLEAN bAbstract
);
```


</dt> </dl> </dd> <dt>

**AuxDerivedFrom**
</dt> <dd> <dl>

Matrice di stringhe ADsPath che indicano le classi ausiliarie Super da cui deriva questa classe.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AuxDerivedFrom(
  [out] VARIANT* pvAuxDerivedFrom
);
HRESULT put_AuxDerivedFrom(
  [in] VARIANT vAuxDerivedFrom
);
```


</dt> </dl> </dd> <dt>

**Ausiliario**
</dt> <dd> <dl>

Valore booleano che indica se questa classe è ausiliaria o meno. Se è **true**, questa classe è una classe ausiliaria e non è possibile crearne un'istanza direttamente nel servizio directory. Le classi ausiliarie possono essere utilizzate solo come classi super di altre classi ausiliarie o come origine di proprietà aggiuntive nelle classi strutturali.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Boolean**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Auxiliary(
  [out] BOOLEAN* pbAuxiliary
);
HRESULT put_Auxiliary(
  [in] BOOLEAN bAuxiliary
);
```


</dt> </dl> </dd> <dt>

**CLSID**
</dt> <dd> <dl>

CLSID facoltativo specifico del provider che identifica l'oggetto COM che implementa questa classe.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CLSID(
  [out] BSTR* pbstrCLSID
);
HRESULT put_CLSID(
  [in] BSTR bstrCLSID
);
```


</dt> </dl> </dd> <dt>

**Contenitore**
</dt> <dd> <dl>

Valore booleano che indica se questa classe può essere un contenitore di altre classi di oggetti. Se questo valore è **true**, è possibile chiamare il metodo **get \_ container** per ottenere una matrice delle classi di oggetti che questa classe può contenere.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Boolean**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Container(
  [out] BOOLEAN* pbContainer
);
HRESULT put_Container(
  [in] BOOLEAN bContainer
);
```


</dt> </dl> </dd> <dt>

**Contenimento**
</dt> <dd> <dl>

Matrice **BSTR** in cui ogni elemento è il nome di una classe di oggetti che questa classe può contenere.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Containment(
  [out] VARIANT* pvContainment
);
HRESULT put_Containment(
  [in] VARIANT vContainment
);
```


</dt> </dl> </dd> <dt>

**Estratta da**
</dt> <dd> <dl>

Matrice di stringhe ADsPath che indicano da quali classi è stata derivata questa classe.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DerivedFrom(
  [out] VARIANT* pvDerivedFrom
);
HRESULT put_DerivedFrom(
  [in] VARIANT vDerivedFrom
);
```


</dt> </dl> </dd> <dt>

**HelpFileContext**
</dt> <dd> <dl>

ID del contesto in **HelpFileName** in cui è possibile trovare informazioni specifiche per questa classe.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileContext(
  [out] long* plHelpContext
);
HRESULT put_HelpFileContext(
  [in] long lHelpContext
);
```


</dt> </dl> </dd> <dt>

**HelpFileName**
</dt> <dd> <dl>

Nome di un file della guida che contiene ulteriori informazioni sugli oggetti di questa classe.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileName(
  [out] BSTR* pbstrHelpFileName
);
HRESULT put_HelpFileName(
  [in] BSTR bstrHelpFileName
);
```


</dt> </dl> </dd> <dt>

**MandatoryProperties**
</dt> <dd> <dl>

**SAFEARRAY** di **varianti** che elenca le proprietà che devono essere impostate affinché questa classe venga scritta nell'archivio. Se la classe contiene solo una proprietà, **get \_ MandatoryProperties** restituirà un **BSTR**.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MandatoryProperties(
  [out] VARIANT* pvarMandatoryProperties
);
HRESULT put_MandatoryProperties(
  [in] VARIANT varMandatoryProperties
);
```


</dt> </dl> </dd> <dt>

**NamingProperties**
</dt> <dd> <dl>

**SAFEARRAY** di **BSTR** che elenca le proprietà utilizzate per denominare gli attributi di questa classe dello schema.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NamingProperties(
  [out] VARIANT* pvarNamingProperties
);
HRESULT put_NamingProperties(
  [in] VARIANT varNamingProperties
);
```


</dt> </dl> </dd> <dt>

**OID**
</dt> <dd> <dl>

Identificatore di oggetto specifico del provider che definisce questa classe. Viene fornito per consentire l'estensione dello schema, utilizzando Active Directory, nei servizi directory che richiedono OID specifici del provider per le classi.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OID(
  [out] BSTR* pbstrOID
);
HRESULT put_OID(
  [in] BSTR bstrOID
);
```


</dt> </dl> </dd> <dt>

**OptionalProperties**
</dt> <dd> <dl>

**SAFEARRAY** di **varianti** che elenca le proprietà facoltative per questa classe dello schema. Se la classe contiene solo una proprietà, **get \_ OptionalProperties** restituirà un **BSTR**.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OptionalProperties(
  [out] VARIANT* pvarOptionalProperties
);
HRESULT put_OptionalProperties(
  [in] VARIANT varOptionalProperties
);
```


</dt> </dl> </dd> <dt>

**PossibleSuperiors**
</dt> <dd> <dl>

Matrice di stringhe ADsPath che indicano le classi dello schema che possono contenere istanze di questa classe.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PossibleSuperiors(
  [out] VARIANT* pvSuperiors
);
HRESULT put_PossibleSuperiors(
  [in] VARIANT vSuperiors
);
```


</dt> </dl> </dd> <dt>

**PrimaryInterface**
</dt> <dd> <dl>

GUID dell'identificatore specifico del provider facoltativo che associa un'interfaccia a oggetti di questa classe dello schema. Ad esempio, la classe "User" che supporta [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) e **PrimaryInterface** è identificata da **IID \_ IADsUser**. Deve essere nel formato stringa standard di un GUID, come definito da COM. Questo GUID è il valore che viene visualizzato nella proprietà [**IADs:: Get \_ GUID**](/windows/desktop/api/Iads/nn-iads-iads) nelle istanze di questa classe per i provider che implementano questa proprietà. L'identificazione di una classe di schema per IID dell'interfaccia principale del codice della classe consente l'utilizzo di **QueryInterface** in fase di esecuzione per determinare se un oggetto è della classe desiderata.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryInterface(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come utilizzare l'interfaccia [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) per determinare se un oggetto può essere un contenitore e, in caso affermativo, elenca i nomi di tutti gli oggetti contenuti.


```VB
Dim ads As IADs
Dim cls As IADsClass

On Error GoTo Cleanup

Set ads = GetObject("WinNT://myComputer,computer")
Set cls = GetObject(ads.Schema)
if cls.Container = True Then
    MsgBox "This object contains the following children:"
    For Each o In cls.Containment
        MsgBox o
    Next
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ads = Nothing
    Set cls = Nothing
```



Nell'esempio di codice seguente viene illustrato come utilizzare l'interfaccia [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) per determinare se un oggetto può essere un contenitore e, in caso affermativo, elenca i nomi di tutti gli oggetti contenuti.


```C++
HRESULT hr = S_OK;
IADsClass *pCls = NULL;
IADs *pADs = NULL;
BSTR bstrSchema;
VARIANT var;
 
hr = CoInitialize(NULL);
hr = ADsGetObject(L"WinNT://myComputer,computer",
                  IID_IADs,
                  (void**)&pADs);
if (FAILED(hr)) {goto Cleanup;}
 
hr = pADs->get_Schema(&bstrSchema);
pADs->Release();
if(FAILED(hr)) {goto Cleanup;}
 
hr = ADsGetObject(bstrSchema, IID_IADsClass, (void**)&pCls);
if(FAILED(hr)) {goto Cleanup;}
 
VariantInit(&var);
VARIANT_BOOL bCont;
pCls->get_Container(&bCont);
if(bCont != false) {
    VariantClear(&var);
    pCls->get_Containment(&var);
    hr = printVarArray(var);
}

Cleanup:
    if(pADs)
        pADs->Release();

    if(pCls)
        pCls->Release();

    SysFreeString(bstrSchema);
    CoUninitialize();
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsClass è definito come C8F93DD0-4AE0-11CF-9E73-00AA004A5691<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[**IADsClass:: Qualifiers**](/windows/desktop/api/Iads/nf-iads-iadsclass-qualifiers)
</dt> </dl>

 

 





