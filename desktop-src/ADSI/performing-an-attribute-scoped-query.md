---
title: Esecuzione di una query sull'ambito degli attributi
description: La query dell'ambito dell'attributo è una preferenza di ricerca che consente di eseguire una ricerca di attributi con valori di nome distinti di un oggetto.
ms.assetid: 026fbe17-5df7-4007-9d74-5c0abbe793b1
ms.tgt_platform: multiple
keywords:
- Esecuzione di una query con ambito di attributo ADSI
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca, query ambito attributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10f5b666028c5fd46e7394b52a1328370e317bc
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300436"
---
# <a name="performing-an-attribute-scope-query"></a>Esecuzione di una query sull'ambito degli attributi

La query dell'ambito dell'attributo è una preferenza di ricerca che consente di eseguire una ricerca di attributi con valori di nome distinti di un oggetto. L'attributo da cercare può essere singolo o multivalore, ma deve essere del tipo di **\_ \_ stringa DN ADS** . Quando viene eseguita la ricerca, ADSI enumera i valori del nome distinto dell'attributo ed esegue la ricerca negli oggetti rappresentati dai nomi distinti. Se, ad esempio, viene eseguita una ricerca con ambito di attributo per l'attributo [**member**](/windows/desktop/ADSchema/a-member) di un oggetto gruppo, ADSI enumera i nomi distinti nell'attributo **member** e cerca i criteri di ricerca specificati in ognuno dei membri del gruppo.

Se una query con ambito di attributo viene eseguita su un attributo che non è di **tipo \_ Ads \_ stringa DN**, la ricerca avrà esito negativo. La query con ambito di attributo richiede anche che la preferenza dell' **\_ ambito di \_ ricerca \_ ADS SEARCHPREF** sia impostata su **Ads \_ scope \_ base**. La preferenza per l' **\_ ambito di \_ ricerca \_ ADS SEARCHPREF** verrà impostata automaticamente sulla **\_ \_ base dell'ambito ADS**, ma se la preferenza per l' **ambito di \_ \_ ricerca \_ ADS SEARCHPREF** è impostata su qualsiasi altro valore, [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) avrà esito negativo con il **\_ \_ \_ parametro E Ads non valido**.

I risultati di una query con ambito attributo possono estendersi su più server e un server non può restituire tutti i dati richiesti per tutte le righe restituite. In tal caso, quando l'ultima riga viene recuperata chiamando [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) o [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow), ADSI restituirà **S \_ Ads \_ ERRORSOCCURRED** anziché **s \_ Ads \_ altre \_ righe**.

Per specificare una query con ambito di attributo, impostare un'opzione di ricerca di query per gli **\_ \_ attributi \_ SEARCHPREF di ADS** con un **ADSTYPE \_ case \_ Ignore valore \_ stringa** impostato su ldapDisplayName dell'attributo per eseguire la ricerca nella matrice [**Ads \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . Questa operazione è illustrata nell'esempio di codice seguente.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBUTE_QUERY;
SearchPref.vValue.dwType = ADSTYPE_CASE_IGNORE_STRING;
SearchPref.vValue.Boolean = L"member";
```



Nell'esempio di codice riportato di seguito viene illustrato come usare l'opzione di ricerca query per l' **\_ \_ attributo \_ SEARCHPREF di ADS** .


```C++
/***************************************************************************

    SearchGroupMembers()

    Searches the members of a group that are of type user and prints each 
    user's cn and distinguishedName values to the console.

    Parameters:

    pwszGroupDN - Contains the distinguished name of the group whose 
    members will be searched.

***************************************************************************/

HRESULT SearchGroupMembers(LPCWSTR pwszGroupDN)
{
    HRESULT hr;
    CComPtr<IDirectorySearch> spSearch;
    CComBSTR sbstrADsPath;
 
    // Bind to the group and get the IDirectorySearch interface.
    sbstrADsPath = "LDAP://";
    sbstrADsPath += pwszGroupDN;
    hr = ADsOpenObject(sbstrADsPath,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IDirectorySearch,
        (void**)&spSearch);
    if(FAILED(hr))
    {
        return hr;
    }
 
    ADS_SEARCHPREF_INFO SearchPrefs[1];

    // Set the ADS_SEARCHPREF_ATTRIBUTE_QUERY search preference.
    SearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_ATTRIBUTE_QUERY;
    SearchPrefs[0].vValue.dwType = ADSTYPE_CASE_IGNORE_STRING;
    SearchPrefs[0].vValue.CaseIgnoreString = L"member";

    // Set the search preferences.
    hr = spSearch->SetSearchPreference(SearchPrefs, sizeof(SearchPrefs)/sizeof(ADS_SEARCHPREF_INFO));
    if(FAILED(hr))
    {
        return hr;
    }

    ADS_SEARCH_HANDLE hSearch;
    
    // Create the search filter.
    LPWSTR pwszSearchFilter = L"(&(objectClass=user))";
 
    // Set attributes to return.
    LPWSTR rgpwszAttributes[] = {L"cn", L"distinguishedName"};
    DWORD dwNumAttributes = sizeof(rgpwszAttributes)/sizeof(LPWSTR);
 
    // Execute the search.
    hr = spSearch->ExecuteSearch(pwszSearchFilter,
        rgpwszAttributes,
        dwNumAttributes,
        &hSearch);
    if(FAILED(hr))
    {
        return hr;
    }

    // Get the first result row.
    hr = spSearch->GetFirstRow(hSearch);
    while(S_OK == hr)
    {
        ADS_SEARCH_COLUMN col;

        // Enumerate the retrieved attributes.
        for(DWORD i = 0; i < dwNumAttributes; i++)
        {
            hr = spSearch->GetColumn(hSearch, rgpwszAttributes[i], &col);
            if(SUCCEEDED(hr))
            {
                switch(col.dwADsType)
                {
                case ADSTYPE_DN_STRING:
                    wprintf(L"%s: %s\n\n", rgpwszAttributes[i], col.pADsValues[0].DNString);
                    break;

                case ADSTYPE_CASE_IGNORE_STRING:
                    wprintf(L"%s: %s\n\n", rgpwszAttributes[i], col.pADsValues[0].CaseExactString);
                    break;

                default:
                    break;
                }
                
                // Free the column.
                spSearch->FreeColumn(&col);
            }
        }
        
        // Get the next row.
        hr = spSearch->GetNextRow(hSearch);
    }

    // Close the search handle to cleanup.
    hr = spSearch->CloseSearchHandle(hSearch);

    return hr;
}
```



Quando questa ricerca viene eseguita e i risultati vengono enumerati, restituisce il **nome**, il **numero di telefono** e il **numero di ufficio** di tutti gli oggetti utente contenuti nell'elenco di attributi **membro** del gruppo.

Gestione degli errori: i risultati di una query con ambito attributo possono estendersi su più server e un server non può restituire tutti i dati richiesti per tutte le righe restituite. In tal caso, quando l'ultima riga viene recuperata chiamando [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) o [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow), ADSI restituirà **s \_ Ads \_ ERRORSOCCURRED**, anziché **s \_ Ads \_ più \_ righe**.

 

 